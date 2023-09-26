# Plano de Gerência e Configuração de Software

Este documento tem como objetivo apresentar as ferramentas, políticas e regras adotadas pelo projeto CAPJu para auxiliar quem deseja contribuir.

## Ferramentas 
| Ferramenta | Finalidade |
|---|---|
| GitHub | Hospedagem e versionamento de código |
| GitHub Actions | Ferramenta de integração contínua |
| GitHub Pages | Hospedagem de página web para repositório GitHub |
| Docker | Ferramenta de isolamento de ambiente |
| Docker-Compose | Ferramenta de gerenciamento de containers |
| Node | Framework utilizado para o desenvolvimento do back-end |
| React | Framework para desenvolvimento Web |
| TypeScript | Linguagem do framework React |
| ESLint | Ferramenta de análise de código TypeScript |
| Prettier | Formatador de código automático |

## Política de Issues
Caso encontre um bug ou tenha alguma sugestão de melhoria para o software, é possível criar uma issue seguindo os passos abaixo:

1. Escolha o tipo de issue a ser criado (funcionalidade, documentação ou correção de bug)
2. Escreva um título sucinto para a issue
3. Preencha a descrição da issue seguindo os passos e as orientações do template
4. Preencha informações adicionais caso possua (executores, épico, marco, história do usuário etc)

Tanto o título como a descrição da issue devem estar escritos em português e seguir suas regras de sintaxe e semântica. 

## Política de Branches

### Repositórios de Código

Para uma mudança chegar a branch master (branch estável) os passos abaixo são seguidos:

1. Toda nova branch deve ser feita a partir da master
2. Ao resolver a issue proposta a nova branch deve ser merjada e comparada em relação a master
3. Caso o PR seja aprovado pela equipe, a nova branch será deletada e seu conteúdo integrado a master

### Repositório de Documentação

Para uma mudança chegar a branch master (branch estável) os passos abaixo são seguidos:

1. Toda nova branch deve ser feita a partir da master
2. Ao resolver a issue proposta, a nova branch deve ser mergeada e comparada em relação a master
3. Caso o PR seja aprovado pela equipe, a nova branch será deletada e seu conteúdo integrado a master

### Regras de Nomenclatura

Toda nova branch criada nos repositórios CAPJu deve se propor a resolver uma issue específica, o nome da branch deve seguir as seguintes regras:

1. Conter o código da issue fornecido pelo GitHub
2. Ser curto e expressivo a respeito da issue a ser tratada
3. As palavras devem ser separadas por hífen "-"
4. Ser escrito em "lower case"

Exemplo: 2-documento-testes

## Política de Commits

Os commits devem ser atômicos (uma contribuição pequena para resolver um problema específico). A mensagem do commit deve relatar o que foi feito de maneira sucinta e direta, começar com um verbo e com a primeira letra maiúscula. Além disso, contribuições feitas por mais de uma pessoa devem conter o comando "Co-authored-by" para identificar todos os autores envolvidos.

Exemplo de contribuição feita por um autor:
```console
    git commit -m "Adicionando nova funcionalidade"
```

Exemplo de contribuição feita por mais de um autor:
```console
    git commit -m "Adicionando uma carta vermelha

    Co-authored-by: Pessoa <GravesEmailGit@email.com>"
```

## Política de Pull Request

Para realizar um Pull Request (PR) para o repositório é necessário seguir os passos abaixo.

1. Ao resolver uma issue, suba suas contribuições e crie um Pull Request
2. Escreva um título sucinto para o PR 
3. Preencha a descrição do PR seguindo os passos e as orientações do template que será mostrado
4. Ligue o PR com a issue que ele resolve
5. Preencha informações adicionais caso possua (executores, revisores, etc)

### Política de Aprovação

Para um Pull Request ser aprovado nos repositórios de código, a contribuição feita deve:

1. Resolver apenas a issue específica ao qual se habilita a tratar
2. Respeitar todos os critérios de aceitação definidos na issue
3. Estar descrita em português
4. Possuir cobertura de testes 
5. Ser aprovada na integração contínua e nas ferramentas que ela executa
6. Conter lógica eficaz para preservar performance do sistema
7. Conter boas práticas de programação para preservar a qualidade do código
8. Não adicionar nenhum comportamento inesperado

Para um Pull Request ser aprovado no repositório de documentação, a contribuição feita deve:

1. Ser relevante para o projeto
2. Resolver apenas a issue específica ao qual se habilita a tratar
3. Respeitar todos os critérios de aceitação definidos na issue
4. Estar na língua portuguesa e seguir as normas desta 
5. Estar na pasta e formato adequados
6. Ser aprovada na integração contínua e nas ferramentas que ela executa

## Política de Documentação

Para contribuir com a documentação do projeto as regras definidas de commit, issue e PR também se aplicam, além destas pedimos atenção aos pontos abaixo:

1. Um novo documento deve ser criado dentro da pasta produto ou projeto, dependendo do que ele trata
2. Todo documento deve iniciar com uma breve explicação do que será tratado
3. Todo documento deverá possuir histórico de versão

Caso o documento seja extenso e possua múltiplos autores um histórico de versão deve ser inserido ao final dele, respeitando as seguintes regras: o versionamento da documentação deve seguir um padrão X.Z, onde X e Z são numerais inteiros não negativos que crescem em ordem crescente. 

Ao fazer grandes incrementos a variável X cresce (1.0, 2.0, 3.0) e ao fazer pequenos incrementos a variável Z cresce (1.1, 1.2, 1.3), ambas variáveis começam em zero e crescem de um em um. Ao subir a versão de X o valor de Z volta pra zero (1.4 -> 2.0). O documento só entra na versão 1.0 se naquele momento ele estiver teoricamente finalizado.

## Continuous Integration/Deployment

### Continuous Integration

### Continuous Deployment

### Pipelines

## Histórico de Versões

| Data | Versão | Descrição | Autor(es) | Revisor(es) |
| ------------- | ------------- | ------------- | ------------- | ------------- | 
| 26/09/2023 | 1.0 | Criação do documento | Brenda Santos, Washington Bispo | A definir |