# Backlog do Produto

O backlog do produto de software pode ser visto como uma lista priorizada de todas as funcionalidades, melhorias e tarefas relacionadas a um produto. Dessa forma, serve como um repositório central para todas as ideias e requisitos do produto, permitindo que a equipe de desenvolvimento e os demais envolvidos gerenciem e planejem o trabalho de forma eficaz. Para isso, o backlog utilizará três principais conceitos: **Épicos** (São itens de alto nível no backlog que representam funcionalidades ou metas de grande escala do produto. São, geralmente, muito amplos e podem não ser facilmente implementados em uma única iteração), **Histórias de usuário** (São unidades menores de trabalho que descrevem funcionalidades ou requisitos específicos do ponto de vista do usuário. Costumam ser mais detalhadas do que épicos e geralmente seguem uma estrutura como "Eu, como [tipo de usuário], quero [realizar uma ação] para poder [atingir um objetivo]") e **Priorização** (Como as histórias e épicos são priorizadas para que o desenvolvimento considere a importância que o cliente dá para cada tópico).

## Priorização - Método MoSCow

Desenvolvida por Dai Clegg durante sua atuação na Oracle na década de 1990, a técnica MoSCoW originou-se no contexto da gestão e dos negócios para aprimorar o processo de desenvolvimento de software. O termo MoSCoW é um acrônimo formado pelas iniciais das categorias "Must Have" (Deve Ter), "Should Have" (Deveria Ter), "Could Have" (Poderia Ter) e "Won't Have" (Não Terá), as quais são utilizadas para segmentar nossas tarefas e determinar suas prioridades:

| Tipo | Descrição |
| :--- | :-------  | 
| Must Have   | “Tem que ser feito” numa tradução literal, seria a categoria para as tarefas mais indispensáveis para o produto, no qual sem elas poderia se considerar um fracasso. |
| Should Have | “Deveria ter”, ou seja, é importante, mas não crucial, por isso são tarefas que devem vir logo após as categorizadas como essenciais.|
| Could Have | “Poderia ter”, tarefas desejáveis, mas que também não necessárias, ou seja, a serem priorizadas apenas se as tarefas das categorias anteriores forem completadas.|
| Won`t Have  | “Não será feito”, tarefas que envolvem muito esforço e têm baixo impacto. Não devem ser priorizadas no momento.|

## Épicos

* [Estatísticas](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/28);
* [Rastreabilidade](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/27);
* [Manutenção de processos](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/18);
* [Exclusão](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/24);
* [Filtros](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/29);
* [_User Experience_](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/30);
* [Segurança](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/26).

## Histórias de Usuário

### [Épico de Estatísticas](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/28)
| ID | Eu, como... | Gostaria de... | Para poder... | Priorização |
|---|---|---|---|---|
| [US01](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/14) | Estagiário, Servidor, Diretor, Juiz, Administrador  | Poder visualizar uma estatística detalhada que mostre a quantidade de processos por etapa. | Ter uma visão clara que exiba a quantidade de processos por etapa, para fácil identificar gargalos, atrasos ou áreas do processo que precisam de atenção especial. | Must |
| [US02](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/22) | Estagiário, Servidor, Diretor, Juiz, Administrador | Ter a capacidade de visualizar uma estatística que apresente a quantidade de processos concluídos dentro de um fluxo. | Monitorar de perto o andamento de processos específicos e avaliar a eficiência do fluxo em questão. | Must |
| [US04](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/31)| Estagiário, Servidor, Diretor, Juiz, Administrador | Ter a capacidade de visualizar o tempo de conclusão de cada etapa de um processo dentro de uma etapa. | Ter as estatísticas do tempo gasto ou atrasos nas etapas. | Must |
| [US05](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/23)| Estagiário, Servidor, Diretor, Juiz, Administrador | Baixar relatório em formato csv e pdf. | Ter a flexibilidade de compartilhar e amazenar os dados de maneira mais conveniente e acessível. | Must |

### [Épico de Rastreabilidade](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/27)
| ID | Eu, como... | Gostaria de... | Para poder... | Priorização |
|---|---|---|---|---|
| [US06](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/21)| Estagiário, Servidor, Diretor, Juiz, Administrador | Visualizar o histórico das mudanças e avanços dos status dos processos. | Acompanhar a rastreabilidade de atividades relacionadas ao processo. | Must |

### [Épico de Manutenção de processos](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/18)
| ID | Eu, como... | Gostaria de... | Para poder... | Priorização |
|---|---|---|---|---|
| [US07](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/12)| Servidor, Diretor, Administrador |  Importar automaticamente os processos através de um arquivo pdf. | Realizar a importação de forma mais prática. | Must |
| [US08](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/17)| Servidor, Diretor, Administrador | Importar automaticamente os processos através de um arquivo csv. | Realizar a importação de forma mais prática. | Must |
| [US09](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/19) | Servidor, Diretor, Administrador | Adicionar um status ao processo. | Visualizar qual o status atual do processo. | Must |

## [Épico de Exclusão](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/24)
| ID | Eu, como... | Gostaria de... | Para poder... | Priorização |
|---|---|---|---|---|
| [US10](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/6) | Servidor, Diretor, Administrador | Excluir um fluxo e todos os processos inclusos nele | Não deixar processos acumulados ou avulsos sem fazer parte de um fluxo. | Must |

### [Épico de Filtros](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/29)
| ID | Eu, como... | Gostaria de... | Para poder... | Priorização |
|---|---|---|---|---|
| [US11](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/7) | Estagiário, Servidor, Diretor, Juiz, Administrador | Filtrar processo através de etapa. | Visualizar quais processos se encontram em uma mesma etapa. | Must |
| [US12](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/10) | Estagiário, Servidor, Diretor, Juiz, Administrador | Filtrar processo por fluxo. | Visualizar quais processos fazem parte do mesmo fluxo. | Must |
| [US14](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/20) | Estagiário, Servidor, Diretor, Juiz, Administrador | Visualizar relatório de processos filtrados pela data de vencimento de uma etapa. | Obter informações dos processos de uma etapa filtrada pela sua data de vencimento. | Must |

### [Épico de _User Experience_](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/30)
| ID | Eu, como... | Gostaria de... | Para poder... | Priorização |
|---|---|---|---|---|
| [US15](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/8) | Estagiário, Servidor, Diretor, Juiz, Administrador | Melhorar feedback de erro. | Entender e contornar possíveis erros. | Should |
| [US16](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/13) | Estagiário, Servidor, Diretor, Juiz, Administrador | Agrupar de forma mais condizente as funcionalidades. | Usar a aplicação com mais facilidade.  | Should |
| [US17](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/16) | Estagiário, Servidor, Diretor, Juiz, Administrador | Melhorar fluxo de exibição das telas. | Usar a aplicação com mais facilidade. | Should |

### [Épico de Segurança](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/26)
| ID | Eu, como... | Gostaria de... | Para poder... | Priorização |
|---|---|---|---|---|
| [US18](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/5) | Estagiário, Servidor, Diretor, Juiz, Administrador | Que minha autenticação seja criptografada de forma segura. | Ter confiança na segurança dos meus dados e informações pessoais, garantindo que apenas eu ou autorizadas tenham acesso ao meu perfil e informações sensíveis. | Should |
| [US19](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/9) | Estagiário, Servidor, Diretor, Juiz, Administrador | Ter as rotas de páginas privadas autenticadas | Garantir a segurança e a privacidade dos dados e dos processos, onde somente usuários autorizados teriam acesso às páginas restritas. | Should |
| [US20](https://github.com/fga-eps-mds/2023-2-CAPJu-Doc/issues/15) | Estagiário, Servidor, Diretor, Juiz, Administrador | Ser deslogado depois de determinado tempo de inatividade. | Evitar acessos de usuários indesejados. | Should |

## Referências
* PEREIRA, Paulo; TORREÃO, Paula; MARÇAL, Ana Sofia. Entendendo Scrum para gerenciar projetos de forma ágil. Mundo PM, v. 1, p. 3-11, 2007.

## Histórico de Versões

| Data | Versão | Descrição | Autor(es) | Revisor(es) |
| ------------- | ------------- | ------------- | ------------- | ------------- | 
| 30/09/2023 | 1.0 | Criação do documento | Brenda, Washington, Denniel, Felipe, Daniel, Davi, João, Leandro | A definir |
| 30/09/2023 | 1.1 | Adição de introdução, referências e links das histórias/épicos | Brenda, Washington, Denniel, Felipe, Daniel, Davi, João, Leandro | A definir |
| 27/11/2023 | 1.2 | Apagando US03 e US13 pois foram canceladas | A definir |

