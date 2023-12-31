# Manual de como executar o CAPJu

## Sistema Operacional

Toda a configuração é feita no Debian 11. Alguns pacotes deb são utilizados
então é recomendado utilizar o mesmo SO para reproduzir a mesma configuração.

```bash
$ lsb_release -a
Distributor ID:	Debian
Description:	Debian GNU/Linux 11 (bullseye)
Release:	11
Codename:	bullseye
```

## Nginx

O Nginx é utilizado como proxy reverso e servidor Web.

Para instalar o Nginx basta instalar seu pacote Debian:

```
$ sudo apt-get install nginx
```

Em seguida, editar o arquivo /etc/nginx/nginx.conf com o seguinte conteúdo:

_OBS_: Se estiver usando uma máquina com outros serviços, é recomendado adaptar
essa configuração para o arquivo /etc/nginx/sites-available/seudominio.com

```
user www-data;
worker_processes auto;
pid /run/nginx.pid;
include /etc/nginx/modules-enabled/*.conf;

events {
  worker_connections 768;
}

http {
  server {
    listen 443 ssl;
    listen [::]:443 ssl;

    server_name capju.sergiosacj.tech 177.93.131.57;

    location / {
      proxy_pass http://localhost:3333;
      proxy_set_header Host $host;
      proxy_set_header X-Real-IP $remote_addr;
      proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    }

    location /prod {
      proxy_pass http://localhost:3000;
      proxy_set_header Host $host;
      proxy_set_header X-Real-IP $remote_addr;
      proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
    }

    ssl_certificate /etc/letsencrypt/live/capju.sergiosacj.tech/fullchain.pem;
    ssl_certificate_key /etc/letsencrypt/live/capju.sergiosacj.tech/privkey.pem;
  }

  server {
    if ($host = capju.sergiosacj.tech) {
      return 301 https://$host$request_uri;
    }

    listen 80;
    listen [::]:80;

    server_name capju.sergiosacj.tech 177.93.131.57;

    return 302 https://$server_name$request_uri;
  }
}
```

Alguns detalhes importantes:

- O nome do server "server_name" é o domínio seguido do IP (HTTPS só irá funcionar com um domínio);
- Para executar mais de uma versão do CAPJu na mesma porta basta configurar diferentes raízes (Exemplo: /dev e /prod);
- A primeira configuração de server é feita para HTTPS, a segunda é feita para redirecionar HTTP para HTTPS;

Após editar o arquivo de configuração do Nginx é importante executar o seguinte comando, para testar se as alterações estão corretas:

```
$ sudo nginx -t
nginx: the configuration file /etc/nginx/nginx.conf syntax is ok
nginx: configuration file /etc/nginx/nginx.conf test is successful
```

Essa configuração ainda não vai funcionar, vamos configurar o certificado TLS antes de reiniciar o servidor do Nginx.

## Let's Encrypt

Pré-requisitos para configurar certificado:

- Domínio registrado;
- O Domínio precisa ter um A record com "seudominio.com" apontando para um IP
  público do servidor (nos exemplos eu uso "capju.sergiosacj.tech" ao invés de
  "seudominio.com");

Sugestão, quem é estudante pode utilizar education.github.com para obter
domínios gratuitamente. Algumas empresas que disponibilizam isso são Tech
Domains, Namecheap, Digital Ocean e outros.

O primeiro passo é instalar o Certbot:

```
$ sudo apt-get install certbot python3-certbot-nginx
```

Se o firewall estiver habilitado, ou seja:

```
$ sudo ufw status
Output
Status: active

To                         Action      From
--                         ------      ----
OpenSSH                    ALLOW       Anywhere
Nginx HTTP                 ALLOW       Anywhere
OpenSSH (v6)               ALLOW       Anywhere (v6)
Nginx HTTP (v6)            ALLOW       Anywhere (v6)
```

é importante permitir HTTPS e remover a permissão para HTTP:

```
$ sudo ufw allow 'Nginx Full'
$ sudo ufw delete allow 'Nginx HTTP'
```

Para checar se está funcionando basta executar o comando status novamente:

```
$ sudo ufw status
Output
Status: active

To                         Action      From
--                         ------      ----
OpenSSH                    ALLOW       Anywhere
Nginx Full                 ALLOW       Anywhere
OpenSSH (v6)               ALLOW       Anywhere (v6)
Nginx Full (v6)            ALLOW       Anywhere (v6)
```

Para obter o certificado usamos o Certbot:

```
$ sudo certbot --nginx -d capju.sergiosacj.tech
```

Esse comando executa o Certbot com o plugin --nginx, usando -d para especificar
os nomes de domínio para os quais gostaríamos que o certificado fosse válido.
Nesse caso, eu especifiquei apenas um subdomínio.

Se esta for a primeira vez que executou o Certbot, você será solicitado a
inserir um endereço de e-mail e concordar com os termos de serviço. Depois de
fazer isso, o Certbot se comunicará com o servidor Let's Encrypt e executará um
desafio para verificar se você controla o domínio para o qual está solicitando
um certificado.

Se for bem-sucedido, o Certbot perguntará como você gostaria de definir suas
configurações de HTTPS.

Após configurado, o Certbot irá indicar o PATH da sua fullchain.pem e da sua
privkey.pem, edite a configuração do Nginx adicionando o seu PATH.

Com isso, podemos reiniciar o Nginx:

```
$ sudo systemctl restart nginx
$ sudo systemctl status nginx # para conferir se está ativo
```

## Configurando a API do CAPJu

Primeiro, é necessário clonar os repositórios do CAPJu: <a href="https://github.com/orgs/fga-eps-mds/teams/2023-2-capju/repositories">https://github.com/orgs/fga-eps-mds/teams/2023-2-capju/repositories.</a>

```
$ sudo apt-get install git
$ git clone https://github.com/fga-eps-mds/2023-2-CAPJu-Note-Service
```

Quando o CAPJu for lançado, é interessante criar um repositório de imagens no
GitLab ou no DockerHub. Desse modo, será possível realizar deploy sem precisar
instalar git na máquina virtual.

Usaremos Docker para realizar o deploy, para instalar basta:

```
$ sudo apt install docker docker-compose
```

Para simplificar o manual, será apresentado como disponibilizar tudo no mesmo
banco, mas a aplicação possui bases de dados independentes. O ideal é
reproduzir esses passos separando os bancos. Não será apresentado essa
separação porque ela simplesmente consiste em replicar o container do postgres.

Primeiro, é necessário configurar todos os .env do repositório, existem
.env-templates, basta criar os .env a partir deles.

Depois basta executar:

```shell
# !/bin/bash

# Lista de serviços.
services=(
  "2023-2-CAPJu-Config"
  "2023-2-CAPJu-User-Service"
  "2023-2-CAPJu-Role-Service"
  "2023-2-CAPJu-Unit-Service"
  "2023-2-CAPJu-ProcessManagement-Service"
  "2023-2-CAPJu-Note-Service"
  "2023-2-CAPJu-Mailer-Service"
)

# Inicia o serviço de configuração.
cd "2023-2-CAPJu-Config"  # Entrar na pasta
  docker-compose up -d
cd ..  # Voltar à pasta anterior

# Espera até que o serviço de configuração esteja online.
while ! docker ps | grep -q db; do
  sleep 1
done

# Inicia os demais serviços.
for service in "${services[@]}"; do
  if [ "${service}" != "2023-2-CAPJu-Config" ]; then
    cd "${service}"
    docker-compose up -d
    cd ..
  fi
done
```

No docker-compose.yml do repositório Config existe um proxy que serve de API Gateway, assim, é
possível acessar todos os microserviços pela mesma porta.

Para executar o Mailer é necessário configurar um servidor SMTP para envio de
e-mail e inserir suas credenciais no seu respectivo .env. O Mailer utiliza o mesmo banco de dados que os outros repositórios, então é necessário o docker config estar rodando para ele conseguir acesso ao banco.

## Configurando o FrontEnd do CAPJu

O FrontEnd do CAPJu utiliza React, criado com Vite e para ser executado necessita primeiro das instalação de suas bibliotecas.

Para isso devemos instalar o [node](https://nodejs.org/en/download) e o gerenciador de pacotes [yarn](https://classic.yarnpkg.com/lang/en/docs/install/#mac-stable). Feito isso, basta rodar o seguinte comando:

```
yarn
```

Com as biblitecas instaladas, crie um arquivo de ambiente e preencha os seguintes valores com as URLs de cada serviço:

```
VITE_USER_SERVICE_URL=
VITE_ROLE_SERVICE_URL=
VITE_UNIT_SERVICE_URL=
VITE_PROCESS_MANAGEMENT_SERVICE_URL=
VITE_NOTE_SERVICE_URL=
```

Para seguir com o desenvolvimento rode:

```
yarn dev
```

Desta forma, tudo já deve estar devidamente configurado.

Para realização de um deploy continuo, recomendamos os serviços da [Netlify](https://www.netlify.com/) que realiza o deploy automático de diversas branches do git de maneira gratuita, além de permitir gerar diferentes ambientes (prod ou dev) e previews das versões de cada pull request.

## Configurando a Interface do CAPJu (FrontEnd)

| Data       | Versão | Descrição                    | Autor(es)       |Revisores|
| ---------- | ------ | ---------------------------- | --------------- |-------------------------|
| 18/12/2023 | 1.0    | Criação do documento | Washington Bispo | Brenda Santos e Leandro Almeida |
