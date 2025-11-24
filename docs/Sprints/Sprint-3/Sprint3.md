# Sprint 3

**Capacidade estimada da equipe por Sprint:** 76 Story Points  
**Meta:** User Stories de rank 7 e rank 11 (Total de 34 Story Points)  
**Previsão da Sprint (extras, sem compromisso de entrega):** User Stories de rank 12 e rank 13 (42 Story Points)

|Rank |Prioridade |Requisito                 |User Story                                                                                                  |Estimativa |Sprint |
|-----|-----------|--------------------------|------------------------------------------------------------------------------------------------------------|-----------|-------|
|7    |Média      |Anexar arquivos           |Eu, como usuários, quero poder anexar arquivos a tarefas, em diferentes formatos                            |13         |3      |
|11   |Baixa      |Visualizar avisos         |Eu, como usuário, quero poder visualizar todas as notificações que foram ligadas ao meu usuário             |21         |3      |
|12   |Baixa      |Progresso do projeto      |Eu, como sistema, desejo informar o andamento do projeto.                                                   |21         |3      |
|13   |Baixa      |Lixeira                   |Eu, como sistema, tenho que salvar todos os itens que forem excluídos.                                      |21         |3      |

# 📉 Cronograma de evolução
![img](../../imgs/Sprint3.png)

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

## User Story 11: Progresso do projeto
**Eu, como usuário, desejo visualizar o progresso total de um projeto.**

- O sistema deve possuir uma barra de progressão em cada projeto, mostrando a porcentagem concluída daquele projeto baseado no número de tarefas
- O sistema deve possuir um gráfico de pizza mostrando quantas de cada tarefas estão nos seguintes estados: Pendente, Em desenvolvimento, Concluídas e Atrasadas

### Casos:
- **Caso 1:** Uma tarefa é adicionada ao projeto
  - O sistema adiciona ao gráfico mais uma tarefa “pendente”
- **Caso 2:** Uma tarefa entra em desenvolvimento
  - O sistema remove seu status atual do gráfico e atualiza para “em desenvolvimento”
- **Caso 3:** Uma tarefa passa de seu prazo de entrega
  - O sistema deve removê-lo de seu status atual do gráfico, caso não esteja em “concluído”, e colocar em “atraso”
- **Caso 4:** Uma tarefa é concluída
  - O sistema remove seu status atual do gráfico e atualiza para “concluído”
  - O sistema aumenta a barra de progressão referente a porcentagem de conclusão do projeto
- **Caso 5:** Uma tarefa é removida de concluído
  - O sistema remove o status de “concluído” do gráfico e coloca no novo status
  - O sistema diminui a barra de progressão referente a porcentagem de conclusão do projeto

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

---

## User Story 13: Lixeira
**Eu, como sistema, deve armazenar todos os arquivos excluídos por um período de tempo antes da exclusão definitiva desse arquivo**

- O sistema deve armazenar o último estado do arquivo na página de “Lixeira”
- O sistema deve retornar o arquivo para o mesmo estado que estava antes da exclusão
- O sistema deve armazenar todos os projetos e tarefas excluídos

### Casos:
- **Caso 1:** Uma tarefa foi excluída
  - O sistema deve armazenar o status da tarefa e os membros responsáveis pela tarefa
- **Caso 2:** Uma tarefa foi restaurada
  - O sistema deve retornar a tarefa para o mesmo local de status junto com os responsáveis pela mesma
- **Caso 3:** Um projeto foi excluído
  - O sistema deve armazenar todos os estados, membros, imagens e tarefas ligadas ao projeto
- **Caso 4:** Um projeto foi restaurado
  - O sistema deve retornar o projeto para o mesmo status, progresso e os arquivos