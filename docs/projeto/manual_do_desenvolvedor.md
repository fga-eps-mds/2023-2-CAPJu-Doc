# Manual do Desenvolvedor

Esse manual tem como objetivo auxiliar você, desenvolvedor, a iniciar e interromper comandos de uma forma mais prática e ágil através de um script. Um exemplo de aplicação seria o comando "docker-compose up -d", onde ao invés de você entrar em todas as pastas e realizar o comando, basta apenas utilizar ele nesses scripts uma vez que irá ser executado em todas as pastas. Primeiramente, para começarmos a utilizar esses scripts, você irá precisar realizar o comando "git clone" dos repositórios do projeto. Posteriormente, siga os passos de cada script para dar continuidade.

## Script 1

O Script 1 tem como objetivo iniciar o comando que você deseja em todos os serviços que estão descritos na Lista de Serviços do script. 

### Passos:

- Crie um arquivo chamado "start_containers.sh" dentro do repositório "2023-2-CAPJu-Doc" e cole o script
- Escreva o comando que você deseja no tópico "Inicia o serviço de configuração" (O comando "docker-compose up -d" é apenas um exemplo de comando, você escolhe qual o comando que você deseja)

```shell
# !/bin/bash

# Lista de serviços.
services=(
  "2023-2-CAPJu-Config"
  "2023-2-CAPJu-Note-Service"
  "2023-2-CAPJu-ProcessManagement-Service"
  "2023-2-CAPJu-Role-Service"
  "2023-2-CAPJu-Unit-Service"
  "2023-2-CAPJu-User-Service"
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

## Script 2

O Script 2 tem como objetivo interromper o comando que está sendo executado em todos os serviços que estão descritos na Lista de Serviços do script. 

### Passos:

- Crie um arquivo chamado "stop_containers.sh" dentro do repositório "2023-2-CAPJu-Doc" e cole o script
- Escreva o comando que você deseja no tópico "Inicia o serviço de configuração" (O comando "docker-compose up -d" é apenas um exemplo de comando, você escolhe qual o comando que você deseja)

```shell
#!/bin/bash

# Lista das pastas
pastas=(
  "2023-2-CAPJu-Config" 
  "2023-2-CAPJu-Note-Service" 
  "2023-2-CAPJu-ProcessManagement-Service" 
  "2023-2-CAPJu-Role-Service" 
  "2023-2-CAPJu-Unit-Service" 
  "2023-2-CAPJu-User-Service"
)

# Loop para entrar em cada pasta e executar o comando docker-compose
for pasta in "${pastas[@]}"; do
  cd "$pasta"  # Entrar na pasta
  docker-compose down
  cd ..  # Voltar à pasta anterior
done
```