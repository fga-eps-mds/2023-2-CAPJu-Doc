# Documento de Arquitetura

# 1. Introdução

## 1.1 Objetivo

&emsp;&emsp;O Documento de arquitetura de software descreve de forma abrangente a arquitetura do projeto, 
com finalidade de compreender e visualizar a estrutura do sistema, suas tecnologias e componentes, apontando 
as decisões arquiteturais da equipe ao longo do desenvolvimento do projeto.

## 1.2 Escopo

&emsp;&emsp;O projeto CAPJu consiste em uma aplicação web que tem como objetivo gerenciar processos jurídicos 
e automatizar tarefas repetitivas que eram realizadas por meio de planilhas, com uma proposta aos usuários poderem 
criar, controlar e acompanhar os processos jurídicos de forma mais eficiente e organizada.
<br>
&emsp;&emsp;Este documento abordará a arquitetura, tecnologias, frameworks e integrações entre os mecanismos 
utilizados no desenvolvimento da aplicação, sendo utilizado para uma gestão eficiente das arquiteturas utilizadas, 
diminuir riscos de conflitos entre as tecnologias utilizadas, além de uma estrutura bem formulada.

## 1.3 Definições, Acrônimos e Abreviações

| Sigla | Descrição |
| :---: | :---: |
| CAPJu | Controle e Acompanhamento de Processos da Justiça |
| HTTP | Hypertext Transfer Protocol |
| API | Application Programming Interface |
| CSS | Cascading Style Sheets |
| JSON | JavaScript Object Notation |

## 1.4 Visão Geral

&emsp;&emsp;O documento foi estruturado da seguinte forma, enquanto detalha os padrões arquiteturais do CAPJu e abordando
as tecnologias utilizadas para o desenvolvimento.

| | Tópico | Descição |
| :---: | :---: | :---: |
| 1 | Introdução | Fornece ao leitor uma visão geral do conteúdo abordado no documento |
| 2 | Representação da Arquitetura | Detalha a arquitetura utilizada no projeto e como ela está organizada |
| 3 | Metas e Restrições da Arquitetura | Descreve os objetivos do projeto, como também suas restrições, do ponto de vista arqutetural |
| 4 | Visão Lógica | Fornece ao leitor uma base para compreender a estrutura e a organização do design do sistema |
| 5 | Visão de Implantação | Fornece ao leitor uma base que permitirá compreender a distribuição física do sistema em um conjunto de nós de processamento |

# 2. Representação da Arquitetura

## 2.1 Tecnologias

&emsp;&emsp;A aplicação utilizadas no desenvolvimento tanto quanto no frontend e no bakcend são as seguintes:

* [Typescript](https://www.typescriptlang.org/): Superconjunto de JavaScript desenvolvido pela Microsoft que adiciona tipagem e alguns outros recursos a linguagem.

* [Jest](https://jestjs.io/): É um framework de teste de JavaScript para gerar testes de forma simples e eficaz.

* [Vite](https://vitejs.dev/): É um build tool que permite que o desenvolvimento de aplicações frontend seja mais rápido e eficiente.

* [React](https://pt-br.reactjs.org/): É uma biblioteca JavaScript de código aberto com foco em criar interfaces de usuário em páginas web.

* [Styled Components](https://styled-components.com/): É uma biblioteca que permite escrever CSS em JavaScript.

* [Node.js](https://nodejs.org/en/): É um ambiente de execução Javascript server-side, utilzando V8.

* [Express](https://expressjs.com/pt-br/): Framework para Node.js que fornece recursos mínimos para construção de servidores web.

* [Sequelize](https://sequelize.org/): É um ORM (Object-Relational Mapping) baseado em promessas para Node.js.

* [PostgreSQL](https://www.postgresql.org/): É um sistema gerenciador de banco de dados objeto relacional.

* [Docker](https://www.docker.com/): Plataforma de software que permite a criação, o teste e a implantação de aplicativos rapidamente.

* [Babel](https://babeljs.io/): Compilador JavaScript gratuito e de código aberto e transpilador de JavaScript usado principalmente para converter o código ECMAScript 2015+ em uma versão compatível com versões anteriores do JavaScript em navegadores ou ambientes atuais e mais antigos.

# 3. Metas e Restrições da Arquitetura

## 3.1 Metas

* Reusabilidade de código
* Baixo acoplamento, facilitando a manutenção futura do código
* Tornar o desenvolvimento do aplicativo mais rápido

## 3.2 Restrições

* Depende de uma conexão com a internet;
* Possuir conexão com o serviço de back-end por API HTTP;
* Possuir conexão com o Banco de Dados.

# 4. Visão Lógica

## 4.1 Visão Geral

O projeto CAPJu utiliza uma arquitetura MVC baseada em microsserviços. A sigla MVC vem dos termos em inglês Model (modelo) View (visão) e Controller (Controle). Essa arquitetura facilita a troca de informações entre a interface do usuário e dados no banco, fazendo com que as respostas sejam mais rápidas e dinâmicas. A base em microsserviços separa a camada de Visão da de Modelo e Controle em programas diferentes e independentes.

O servidor é dividido em 6 microsserviços, sendo eles: [user](https://github.com/fga-eps-mds/2023-2-CAPJu-User-Service), [unit](https://github.com/fga-eps-mds/2023-2-CAPJu-Unit-Service), [processManagement](https://github.com/fga-eps-mds/2023-2-CAPJu-ProcessManagement-Service), [role](https://github.com/fga-eps-mds/2023-2-CAPJu-Role-Service), [note](https://github.com/fga-eps-mds/2023-2-CAPJu-Note-Service) e [mailer](https://github.com/fga-eps-mds/2023-2-CAPJu-Mailer-Service); sendo eles para gerenciamento de usuários, gerenciamento de unidades, gerenciamento de processos, fluxos e etapas, gerenciamento de cargos e permissões, gerenciamento de notas como comentários e auditorias, e gerenciamento de e-mail e notificações, respectivamente.

O repositório [Config](https://github.com/fga-eps-mds/2023-2-CAPJu-Config) é responsável por abrigar configurações do Nginx (funcionando como um proxy reverso) e do Banco de Dados.

# 5. Visão de Implantação

## 5.1 Diagrama de Entidade e Relacionamento

O Diagrama de Entidade-Relacionamento é uma ferramenta utilizada para modelar dados num sistema de informação. Ele representa graficamente as entidades do sistema, bem como os relacionamentos entre elas.

O DER é composto por entidades, atributos e relacionamentos, que são representados por meio de símbolos específicos. As entidades representam os objetos principais do sistema, como unidades, pessoas, fluxos e processos. Os atributos são características desses objetos, como nome por exemplo. Já os relacionamentos indicam como as entidades estão relacionadas entre si, como um processo que está no fluxo.

![Diagrama de Entidade e Relacionamento](../assets/Diagrams/der.jpeg)

<!-- Possíveis mais tópicos -->

## 5.2 Diagrama de Pacotes

O diagrama de pacotes é uma ferramenta da UML que apresenta a estrutura do sistema em relação aos pacotes utilizados em sua organização. Por meio desse artefato, é possível obter uma visão hierárquica dos elementos da aplicação. O diagrama de pacotes é composto por diferentes elementos, como pacotes, elementos empacotados, dependências, importações de elementos e pacotes, bem como a mesclagem de pacotes.

<iframe frameborder="0" style="width:100%;height:673px;" src="https://viewer.diagrams.net/?tags=%7B%7D&highlight=0000ff&edit=_blank&layers=1&nav=1&title=diagrama%20capju%202023-2#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1STCP21LkQ1U3syxksoNX5z3T8mwnZG41%26export%3Ddownload"></iframe>

# Referências

# Histórico de Versões

| Data | Versão | Descrição | Autor(es) |
| :---: | :---: | :---: | :---: |
| 21/10/2023 | 0.1.0 | Criação do documento | Felipe Motta e Nícolas Georgeos |
| 20/12/2023 | 0.1.1 | Atualização do documento | Brenda Santos e Washington Bispo |
