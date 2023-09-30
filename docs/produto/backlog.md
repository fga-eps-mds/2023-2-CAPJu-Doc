# Backlog do Produto


## Priorização - Método MoSCow

Desenvolvida por Dai Clegg durante sua atuação na Oracle na década de 1990, a técnica MoSCoW originou-se no contexto da gestão e dos negócios para aprimorar o processo de desenvolvimento de software. O termo MoSCoW é um acrônimo formado pelas iniciais das categorias "Must Have" (Deve Ter), "Should Have" (Deveria Ter), "Could Have" (Poderia Ter) e "Won't Have" (Não Terá), as quais são utilizadas para segmentar nossas tarefas e determinar suas prioridades:

| Tipo | Descrição |
| :--- | :-------  | 
| Must Have   | “Tem que ser feito” numa tradução literal, seria a categoria para as tarefas mais indispensáveis para o produto, no qual sem elas poderia se considerar um fracasso. |
| Should Have | “Deveria ter”, ou seja, é importante, mas não crucial, por isso são tarefas que devem vir logo após as categorizadas como essenciais.|
| Could Have | “Poderia ter”, tarefas desejáveis, mas que também não necessárias, ou seja, a serem priorizadas apenas se as tarefas das categorias anteriores forem completadas.|
| Won`t Have  | “Não será feito”, tarefas que envolvem muito esforço e têm baixo impacto. Não devem ser priorizadas no momento.|

## Épicos

* Estatísticas;
* Rastreabilidade;
* Manutenção de processos;
* Exclusão;
* Filtros;
* _User Experience_;
* Segurança.

## Histórias

### Épico de Estatísticas (fazendo)
| ID | Eu, como... | Gostaria de... | Para poder... | Priorização |
|---|---|---|---|---|
| [US01](https://github.com/fga-eps-mds/) | Estagiário, Servidor, Diretor, Juiz, Administrador  | Poder visualizar uma estatística detalhada que mostre a quantidade de processos por etapa. | Ter uma visão clara que exiba a quantidade de processos por etapa, para fácil identificar gargalos, atrasos ou áreas do processo que precisam de atenção especial. | Must |
| [US02](https://github.com/fga-eps-mds/) | Estagiário, Servidor, Diretor, Juiz, Administrador | Ter a capacidade de visualizar uma estatística que apresente a quantidade de processos concluídos dentro de um fluxo. | Monitorar de perto o andamento de processos específicos e avaliar a eficiência do fluxo em questão. | Must |
| [US03](https://github.com/fga-eps-mds/)| Estagiário, Servidor, Diretor, Juiz, Administrador |  Ter a capacidade de visualizar as estatísticas detalhadas sobre um processo específico. | Avaliar o processo em profundidade, entender seu status atual e fazer melhorias informadas. | Must |
| [US04](https://github.com/fga-eps-mds/)| Estagiário, Servidor, Diretor, Juiz, Administrador | Ter a capacidade de visualizar o tempo de conclusão de cada etapa de um processo dentro de uma etapa. | Ter as estatísticas do tempo gasto ou atrasos nas etapas. | Must |
| [US05](https://github.com/fga-eps-mds/)| Estagiário, Servidor, Diretor, Juiz, Administrador | Baixar relatório em formato csv e pdf. | Ter a flexibilidade de compartilhar e amazenar os dados de maneira mais conveniente e acessível. | Must |

### Épico de Rastreabilidade (feito)
| ID | Eu, como... | Gostaria de... | Para poder... | Priorização |
|---|---|---|---|---|
| [US06](https://github.com/fga-eps-mds/)| Estagiário, Servidor, Diretor, Juiz, Administrador | Visualizar o histórico das mudanças e avanços dos status dos processos. | Acompanhar a rastreabilidade de atividades relacionadas ao processo. | Must |

### Épico de Manutenção de processos
| ID | Eu, como... | Gostaria de... | Para poder... | Priorização |
|---|---|---|---|---|
| [US07](https://github.com/fga-eps-mds/)| Servidor, Diretor, Administrador |  Importar automaticamente os processos através de um arquivo pdf. | Realizar a importação de forma mais prática. | Must |
| [US08](https://github.com/fga-eps-mds/)| Servidor, Diretor, Administrador | Importar automaticamente os processos através de um arquivo csv. | Realizar a importação de forma mais prática. | Must |
| [US09](https://github.com/fga-eps-mds/) | Servidor, Diretor, Administrador | Adicionar um status ao processo. | Visualizar qual o status atual do processo. | Must |

## Épico de Exclusão
| ID | Eu, como... | Gostaria de... | Para poder... | Priorização |
|---|---|---|---|---|
| [US10](https://github.com/fga-eps-mds/) | Servidor, Diretor, Administrador | Excluir um fluxo e todos os processos inclusos nele | Não deixar processos acumulados ou avulsos sem fazer parte de um fluxo. | Must |

### Épico de Filtros
| ID | Eu, como... | Gostaria de... | Para poder... | Priorização |
|---|---|---|---|---|
| [US11](https://github.com/fga-eps-mds/) | Estagiário, Servidor, Diretor, Juiz, Administrador | Filtrar processo através de etapa. | Visualizar quais processos se encontram em uma mesma etapa. | Must |
| [US12](https://github.com/fga-eps-mds/) | Estagiário, Servidor, Diretor, Juiz, Administrador | Filtrar processo por fluxo. | Visualizar quais processos fazem parte do mesmo fluxo. | Must |
| [US13](https://github.com/fga-eps-mds/) | Estagiário, Servidor, Diretor, Juiz, Administrador | Visualizar processos na etapa de um fluxo. | Acessar quais processos se encontram em determinada etapa de um fluxo. | Must |
| [US14](https://github.com/fga-eps-mds/) | Estagiário, Servidor, Diretor, Juiz, Administrador | Visualizar relatório de processos filtrados pela data de vencimento de uma etapa. | Obter informações dos processos de uma etapa filtrada pela sua data de vencimento. | Must |

### Épico de _User Experience_
| ID | Eu, como... | Gostaria de... | Para poder... | Priorização |
|---|---|---|---|---|
| [US15](https://github.com/fga-eps-mds/) | Estagiário, Servidor, Diretor, Juiz, Administrador | Melhorar feedback de erro. | Entender e contornar possíveis erros. | Should |
| [US16](https://github.com/fga-eps-mds/) | Estagiário, Servidor, Diretor, Juiz, Administrador | Agrupar de forma mais condizente as funcionalidades. | Usar a aplicação com mais facilidade.  | Should |
| [US17](https://github.com/fga-eps-mds/) | Estagiário, Servidor, Diretor, Juiz, Administrador | Melhorar fluxo de exibição das telas. | Usar a aplicação com mais facilidade. | Should |

### Épico de Segurança
| ID | Eu, como... | Gostaria de... | Para poder... | Priorização |
|---|---|---|---|---|
| [US18](https://github.com/fga-eps-mds/) | Estagiário, Servidor, Diretor, Juiz, Administrador | Que minha autenticação seja criptografada de forma segura. | Ter confiança na segurança dos meus dados e informações pessoais, garantindo que apenas eu ou autorizadas tenham acesso ao meu perfil e informações sensíveis. | Should |
| [US19](https://github.com/fga-eps-mds/) | Estagiário, Servidor, Diretor, Juiz, Administrador | Ter as rotas de páginas privadas autenticadas | Garantir a segurança e a privacidade dos dados e dos processos, onde somente usuários autorizados teriam acesso às páginas restritas. | Should |
| [US20](https://github.com/fga-eps-mds/) | Estagiário, Servidor, Diretor, Juiz, Administrador | Ser deslogado depois de determinado tempo de inatividade. | Evitar acessos de usuários indesejados. | Should |

## Histórico de Versões

| Data | Versão | Descrição | Autor(es) | Revisor(es) |
| ------------- | ------------- | ------------- | ------------- | ------------- | 
| 30/09/2023 | 1.0 | Criação do documento | Brenda, Washington, Denniel, Felipe, Daniel, Davi, João, Leandro | A definir |

