# Plano de Gerenciamento de Riscos

O plano de gerenciamento de riscos é uma ferramenta essencial em projetos, negócios e operações que visa auxiliar na identificação, avaliação, mitigação e monitoramento dos riscos potenciais que podem afetar um objetivo ou o projeto por completo. Para isso, os riscos são categorizados, analisados quanto ao impacto e prioridade, descritos de acordo com suas características e formas de mitigação/prevenção.

## Categoria de Riscos

Ambiguidades na execução de um projeto surgem a partir de circunstâncias incertas que têm o potencial de impactar positivamente ou negativamente os resultados almejados. Dada a diversidade de fatores que podem influenciar tais ocorrências, foi adotada uma abordagem que agrupa esses eventos incertos em quatro amplas categorias, são elas:

* **Técnico:** Abordam tecnologia, requisitos, complexidade, desempenho, interfaces, confiabilidade e qualidade.
* **Externo:** Abordam riscos relativos ao cliente, mercado, ambiente de trabalho e fatores pessoais.
* **Organizacional:** Abordam a priorização, recursos e dependências do projeto.
* **Gerência:** Abordam planejamento, controle, estimativa e comunicação.

## Análise Quantitativa

### Probabilidade

**Probabilidade** | **Intervalo** | **Peso**
:---------------: | :-----------: | :------:
**Muito Alta**    |   81% a 100%    |    5
**Alta**          |   61% a 80%     |    4
**Média**         |   41% a 60%     |    3
**Baixa**         |   21% a 40%     |    2
**Muito Baixa**   |   0% a 20%      |    1

### Impacto

Para se quantificar o impacto do risco no projeto o custo, o tempo, o escopo e a qualidade devem ser levados em conta.

**Impacto**       |                     **Descrição**                      | **Peso**
:---------------: | :----------------------------------------------------: | :------:
**Muito Alto**    | O impacto inviabiliza o projeto                        |    5
**Alto**          | Há grande impacto no desenvolvimento do projeto        |    4
**Médio**         | Possui certo impacto porém é facilmente recuperado     |    3
**Baixo**         | Pouco impacto no desenvolvimento do projeto            |    2
**Muito Baixo**   | Impacto pouco expressivo no desenvolvimento do projeto |    1

### Prioridade

Através da multiplicação entre as estimativas de impacto e probabilidade é possível calcular a prioridade dos riscos. A partir desses valores é determinada a urgência da inicialização de medidas de mitigação e resolução dos riscos.

**Probabilidade x Impacto** | **Muito Baixo** | **Baixo** | **Médio**  | **Alto** | **Muito Alto**
:-----------------------: | :-------------: | :-------: |:----------:|:--------:|:------------: 
**Muito Baixa**           |        1        |    2      |      3     |    4     |      5
**Baixa**                 |        2        |    4      |      6     |    8     |      10
**Média**                 |        3        |    6      |      9     |    12    |      15
**Alta**                  |        4        |    8      |      12    |    16    |      20
**Muito Alta**            |        5        |    10     |      15    |    20    |      25

#### Valor de Prioridade

**Prioridade** | **Intervalo** 
:------------: | :-----------: 
**Muito Alta** |     21 a 25    
**Alta**       |     16 a 20   
**Média**      |     11 a 15     
**Baixa**      |     6 a 10   
**Muito Baixa**|     1 a 5      

## Identificação dos Riscos

### R01 - Divergência de horários entre membros da equipe
**Categoria:** Gerência  
**Causa:** Membros com grades horárias muito distintas  
**Consequência:** Dificuldade para reunir toda a equipe e realizar os pareamentos  
**Ação Preventiva:** Elaboração de planilhas de controle de horários  
**Ação Reativa:** Planejar os pareamentos e reuniões baseado na planilha de horários   

### R02 - Dificuldades da equipe com as novas tecnologias inseridas
**Categoria:** Técnico  
**Causa:** Inexperiência de alguns membros  
**Consequência:** Surgimento de dívidas técnicas pela dificuldade em realizar os objetivos propostos  
**Ação Preventiva:** Realização de treinamentos efetivos nas tecnologias a serem utilizadas ao longo do semestre      
**Ação Reativa:** Organizar pareamento para rotação do conhecimento    

### R03 - Falta de comprometimento dos membros com o projeto
**Categoria:** Gerência  
**Causa:** Desânimo com o curso, problemas pessoais ou de saúde, excesso de compromissos, entre outros  
**Consequência:** Issues não entregues, dívida técnica e replanejamento               
**Ação Preventiva:** Motivar os membros do grupo e não permitir que o trabalho se torne tão massante      
**Ação Reativa:** Reorganizar o cronograma e entender o motivo da falta de comprometimento para tentar evitar que ele se repita    

### R04 - Problemas pessoais ou de saúde   
**Categoria:** Externo    
**Causa:** Problemas pessoais/doenças dos membros da equipe  
**Consequência:** Capacidade de trabalho da equipe prejudicada e atrasos no cronograma   
**Ação Preventiva:** Manter uma boa comunicação entre os integrantes  
**Ação Reativa:** Remanejamento das atividades e apoio ao(s) membro(s) afetado(s)   

### R05 - Erros durante o planejamento das atividades   
**Categoria:** Gerência   
**Causa:** Falta de experiência da equipe de gerência  
**Consequência:** Trabalho mal distribuído entre os membros da equipe   
**Ação Preventiva:** Conhecer bem a capacidade da equipe e as necessidades do projeto    
**Ação Reativa:**  Avaliar as métricas e prioridades do projeto para regular os próximos planejamentos   

### R06 - Falta de foco dos membros nas reuniões    
**Categoria:** Gerência     
**Causa:** Diversas distrações em um contexto de reuniões (principalmente) remotas   
**Consequência:** Reuniões longas e com pouca produtividade        
**Ação Preventiva:** Criar timebox para os tópicos da reunião e permanecer nos assuntos que são de interesse geral    
**Ação Reativa:** Mudar a maneira como a reunião é conduzida  

### R07 - Conflito com outras disciplinas   
**Categoria:** Organizacional    
**Causa:** Necessidade, sendo alunos da UnB os membros da equipe precisam cursar outras disciplinas para conclusão da graduação    
**Consequência:** Falta de tempo para se dedicar ao projeto   
**Ação Preventiva:** Enfatizar e auxiliar boa gestão do tempo dos membros    
**Ação Reativa:** Organização do tempo disponível para as disciplinas   

### R08 - Alteração do escopo   
**Categoria:** Gerência    
**Causa:** Surgimento de novos requisitos    
**Consequência:** Replanejamento do projeto     
**Ação Preventiva:** Refinar constantemente os requisitos e manter validações constantes   
**Ação Reativa:** Redefinir o escopo e redistribuir tarefas     

### R09 - Ausência de membros durante reuniões do grupo   
**Categoria:** Gerência     
**Causa:** Membros sobrecarregados ou desestimulados com o projeto     
**Consequência:** Membros perdidos na sprint e maior carga de trabalho para o restante da equipe     
**Ação Preventiva:** Manter a equipe estimulada e verificar constatemente os horários para que não haja conflito      
**Ação Reativa:** Repassar o conteúdo da reunião aos membros faltantes         

### R10 - Conflito de dependência entre atividades
**Categoria:** Organizacional   
**Causa:** Escopo do projeto é muito específico e os membros não têm familiaridade    
**Consequência:** Atividade pausada esperando a conclusão de outra, criando possíveis gargalos        
**Ação Preventiva:** Planejar e priorizar as tarefas a longo prazo, com muita atenção    
**Ação Reativa:** Finalizar uma das tarefas o mais rápido possível para que a outra possa ser realizada        

### R11 - Desistência da disciplina          
**Categoria:** Gerência    
**Causa:** Sobrecarga, problemas pessoais ou de saúde, entre outros       
**Consequência:** Equipe desfalcada e sobrecarga dos membros que permanecem na matéria      
**Ação Preventiva:** Incentivar a participação dos membros e a união do time      
**Ação Reativa:** Redistribuir tarefas e refazer parte do planejamento do projeto    

### R12 - Problemas com a estação de trabalho        
**Categoria:** Técnico     
**Causa:** Falta de acesso a uma boa internet e/ou a um computador funcionando    
**Consequência:** Capacidade de trabalho da equipe prejudicada e atrasos no cronograma     
**Ação Preventiva:** -    
**Ação Reativa:**  Remanejamento das atividades e revisão do cronograma    

### R13 - Alteração das tecnologias    
**Categoria:** Técnico      
**Causa:** Tecnologia previamente escolhida não consegue suprir as necessidades do projeto    
**Consequência:** Refatorar tudo o que foi feito na nova linguagem/framework escolhido      
**Ação Preventiva:** Estudar com antecedência as tecnologias utilizadas e suas capacidades     
**Ação Reativa:** Incluir todos os membros na refatoração para que ela seja executada o mais rápido possivel    

### R14 - Falta de validação de artefatos com cliente    
**Categoria:** Gerência     
**Causa:**  Falta de tempo da equipe ou do cliente para realizar a validação com a recorrência devida    
**Consequência:**  A criação de um artefato que não tem atende ao seu propósito    
**Ação Preventiva:** Validar e comunicar qualquer ação/tarefa previamente com o cliente    
**Ação Reativa:** Validar com o cliente as atividades    

## Comportamento dos Riscos

No desfecho da etapa de desenvolvimento da aplicação, os riscos já foram devidamente identificados, monitorados e, quando viável, tratados de maneira abrangente. Com todo o registro da evolução ou involução desses riscos em mãos, é possível estabelecer correlações entre a fase atual do projeto e a dinâmica dos riscos. O propósito principal é ter registros dos possíveis riscos, como mitiga-los ou gerencia-los e expor de forma clara e simplificada a evolução ao longo das etapas, razão pela qual foram confeccionadas tabelas que destacam as prioridades atribuídas a cada risco em cada fase, acompanhadas dos respetivos gráficos de redução de riscos.

### Técnico

Período   | Dificuldades da equipe com novas tecnologias inseridas | Problemas com a estação de trabalho | Alteração das tecnologias
:--------:| :----------------------------------------------------: | :---------------------------------: | :------------------------:
Semana 1     | 6 | 6 | 1 |
Semana 2     | 6 | 6 | 1 |
Semana 3     | 6 | 6 | 1 |
Semana 4     | 6 | 6 | 1 |
Semana 5     | 6 | 6 | 1 |
Semana 6     | 6 | 6 | 1 |
Semana 7     | 6 | 6 | 1 |
Sprint 1     | 20 | 9 | 1 |
Sprint 2     | 20 | 9 | 1 |
Sprint 3     | 15 | 9 | 1 | 
Sprint 4     | 12 | 9 | 1 | 
Sprint 5     | 12 | 9 | 1 | 
Sprint 6     | 3 | 9 | 5 | 
Sprint 7     | 3 | 9 | 5 | 
Sprint 8     | 3 | 9 | 5 | 
Sprint 9     | 3 | 9 | 5 | 

### Externo

Período   | Problemas pessoais ou de saúde |
:--------:| :-----------------: |
Semana 1     | 9 |
Semana 2     | 9 |
Semana 3     | 9 |
Semana 4     | 9 |
Semana 5     | 9 |
Semana 6     | 9 |
Semana 7     | 9 |
Sprint 1     | 9 | 
Sprint 2     | 9 |
Sprint 3     | 9 |  
Sprint 4     | 9 |  
Sprint 5     | 9 |  
Sprint 6     | 9 |
Sprint 7     | 9 |
Sprint 8     | 9 |
Sprint 9     | 9 |

### Organizacional

Período   | Conflito com outras disciplinas | Conflito de dependência entre atividades |
:--------:| :--------------------------: | :-------------------------: |
Semana 1     | 9 | 12 | 
Semana 2     | 9 | 12 | 
Semana 3     | 9 | 12 | 
Semana 4     | 9 | 12 | 
Semana 5     | 9 | 12 | 
Semana 6     | 9 | 12 | 
Semana 7     | 9 | 12 |                
Sprint 1     | 9 | 6 |
Sprint 2     | 8 | 6 | 
Sprint 3     | 4 | 5 |                                         
Sprint 4     | 4 | 5 |                                         
Sprint 5     | 8 | 5 | 
Sprint 6     | 8 | 5 |  
Sprint 7     | 15 | 4 |  
Sprint 8     | 15 | 4 |  
Sprint 9     | 15 | 4 |                                          

### Gerência

Período | Divergência de horários entre membros da equipe | Falta de comprometimento dos membros com o projeto | Erros durante o planejamento das atividades | Falta de foco dos membros nas reuniões | Alteração do escopo | Ausência de membros durante reuniões do grupo | Desistência da disciplina | Falta de validação de artefatos com cliente |         
:-------: |:-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: | :-------: |           
Semana 1     | 5 | 8 | 15 | 20 | 10 | 6 | 4 | 6 | 
Semana 2     | 5 | 8 | 15 | 20 | 10 | 6 | 4 | 6 | 
Semana 3     | 5 | 8 | 15 | 20 | 10 | 6 | 4 | 6 | 
Semana 4     | 5 | 8 | 15 | 12 | 10 | 6 | 4 | 6 | 
Semana 5     | 5 | 8 | 15 | 12 | 10 | 6 | 4 | 6 | 
Semana 6     | 10 | 8 | 15 | 12 | 10 | 6 | 4 | 6 | 
Semana 7     | 10 | 8 | 15 | 12 | 10 | 6 | 4 | 6 |                 
Sprint 1     | 10 | 8 | 20 | 8 | 10 | 6 | 4 | 12 | 
Sprint 2     | 12 | 8 | 20 | 8 | 10 | 6 | 4 | 12 | 
Sprint 3     | 12 | 8 | 12 | 8 | 10 | 6 | 2 | 6 |                                     
Sprint 4     | 12 | 8 | 12 | 8 | 10 | 6 | 2 | 6 |                                     
Sprint 5     | 12 | 8 | 12 | 8 | 10 | 6 | 2 | 4 |  
Sprint 6     | 12 | 8 | 12 | 8 | 10 | 6 | 2 | 4 |
Sprint 7     | 12 | 16 | 8 | 6 | 5 | 10 | 3 | 16 |
Sprint 8     | 12 | 16 | 8 | 6 | 5 | 10 | 3 | 16 |
Sprint 9     | 12 | 16 | 8 | 6 | 5 | 10 | 3 | 16 |                                   

## Referências

* RODRIGUES, Eli. EAR para projetos de software. Disponível em [https://www.elirodrigues.com/2013/09/21/gerenciamento-de-riscos-ear-para-projetos-de-software/](https://www.elirodrigues.com/2013/09/21/gerenciamento-de-riscos-ear-para-projetos-de-software/). Acesso em 20 set 2023.

## Histórico de Versões

| Data | Versão | Descrição | Autor(es) | Revisor(es) |
| ------------- | ------------- | ------------- | ------------- | ------------- | 
| 26/09/2023 | 1.0 | Criação do documento | Brenda Santos, Washington Bispo | A definir |
| 02/11/2023 | 1.1 | Atualizando tabelas de riscos até a sprint 3 | Brenda Santos, Washington Bispo | Leandro Almeida e Camila Careli |
| 13/11/2023 | 1.2 | Atualizando tabelas de riscos até a sprint 4 e 5 | Denniel William | Brenda Santos, Washington Bispo |
| 20/12/2023 | 1.3 | Atualizando tabelas de riscos até a sprint 9 | Brenda Santos, Washington Bispo | A definir |