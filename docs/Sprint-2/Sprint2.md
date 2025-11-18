# Sprint 2

**Capacidade estimada da equipe por Sprint:** 68 Story Points  
**Meta:** User Stories de rank 9 e rank 7 (Total de 47 Story Points)  
**Previsão da Sprint (extras, sem compromisso de entrega):** User Stories de rank 8 e rank 12 (21 Story Points)

|Rank |Prioridade |Requisito                 |User Story                                                                                                  |Estimativa |Sprint |
|-----|-----------|--------------------------|------------------------------------------------------------------------------------------------------------|-----------|-------|
|9    |Média      |Calendário do projeto     |Eu, como usuário, quero visualizar um calendário de entrega do projeto.                                     |34         |2      |
|7    |Média      |Anexar arquivos           |Eu, como usuários, quero poder anexar arquivos a tarefas, em diferentes formatos                            |13         |2      |
|8    |Média      |Registro de entregas próximas|Eu, como sistema, quero informar ao usuário as tarefas com os prazos mais próximos                          |8          |2      |
|12   |Média      |Tarefas por membros       |Eu, como sistema, desejo informar quantas tarefas foram concluídas por cada um dos membros de um projeto    |13         |2      |

## User Story 7: Anexo de Arquivos
**Eu, como usuários, quero poder anexar arquivos a tarefas, em diferentes formatos** 

- O usuário deve conseguir arquivos a tarefas no formato de: PDF, Png, Jpeg, Docs e Mp4
- O tamanho máximo de arquivo que o usuário pode subir é de 50mb
- O sistema deve exigir para a entrega de uma tarefa seja feito um anexo de pelo menos 1 arquivo
- O usuário deve conseguir visualizar todos os arquivos anexados a uma tarefa

### Casos:
- **Caso 1:** O usuário anexou um arquivo válido ao concluir a tarefa
  - O sistema permite a conclusão da tarefa mudando seu status para “concluido”
- **Caso 2:** O usuário não anexou um arquivo ao concluir a tarefa
  - O sistema não permite a conclusão da tarefa, informando que pelo 1 arquivo deva ser anexado a tarefa para concluí la

### Testes:
- **Teste 1:** O usuário anexou um arquivo em um formato invalido
  - O sistema não permite a anexação do arquivo, pedindo que coloque um arquivo nos formatos válidos

---

## User Story 8: Registro de próximas entregas
**Eu, como usuário, quero visualizar as tarefas atribuídas a mim com os prazos mais próximos**

- O usuário deve possuir uma página própria mostrando quais são suas tarefas com os prazos mais próximos
- O sistema deve direcionar o usuário até o projeto que uma tarefa pertence ao selecioná la

### Casos:
- **Caso 1:** Uma tarefa está próxima da entrega
  - Os usuários atribuídos a essa tarefa poderão ver que sou prazo está próximo
- **Caso 2:** O usuário seleciona uma tarefa em sua página de próximas entregas
  - O usuário será redirecionado para a página do projeto correspondente aquela tarefa

---

## User Story 9: Calendário
**Eu, como usuário, quero visualizar um calendário de entregas do projeto.**

- O sistema deve possuir um calendário geral de projetos, listando o prazo de todas as atividades do projeto selecionado
- O sistema deve possuir um calendário apenas do usuário, referentes as tarefas dele ao projeto selecionado
- O usuário deve ser capaz de mudar entre o calendário do projeto e o calendário pessoal

### Casos:
- **Caso 1:** Uma nova tarefa é criada por um usuário
  - O sistema coloca a tarefa no calendário do projeto referente ao dia do prazo atribuído a ela
- **Caso 2:** Uma tarefa é atribuída a um usuário
  - O sistema coloca a tarefa no calendário pessoal referente ao dia do prazo atribuído a ela
- **Caso 3:** O usuário seleciona qual calendário deseja visualizar
  - O sistema alterna entre os dois tipos de calendários selecionados

---

## User Story 12: Tarefas por membros
**Eu, como sistema, desejo informar quantas tarefas foram concluídas por cada um dos membros de um projeto**

- O sistema deve possuir um gráfico de barras que mostre quantas tarefas foram alocadas para cada membro da equipe, mostrando os membros com mais tarefas na equipe
 
### Casos:
- **Caso 1:** Uma tarefa é atribuída a um membro
  - O sistema registra essa tarefa ao número total de tarefas do usuário
- **Caso 2:** Uma tarefa é removida da atribuição a um membro 
  - O sistema remove essa tarefa e atualiza o total de tarefas do usuário
- **Caso 3:** Após atribuir uma tarefa a um membro ele fica com mais tarefas que outros usuários
  - O sistema substitui no gráfico mostrando o novo usuários com mais tarefas atribuídas
