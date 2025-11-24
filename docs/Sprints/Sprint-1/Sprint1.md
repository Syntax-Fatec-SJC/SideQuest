# Sprint 1

**Capacidade estimada da equipe por Sprint:** 42 Story Points  
**Meta:** User Stories de rank 3 e rank 6 (Total de 13 Story Points)  
**Previsão da Sprint (extras, sem compromisso de entrega):** User Stories de rank 1, rank 2, rank 4 e rank 5 (28 Story Points)

|Rank |Prioridade |Requisito                 |User Story                                                                                                  |Estimativa |Sprint |
|-----|-----------|--------------------------|------------------------------------------------------------------------------------------------------------|-----------|-------|
|3    |Alta       |Gerenciamento de projetos |Eu, como usuário, desejo visualizar todos os projetos que estão em aberto ou finalizados, podendo adicionar ou excluir projetos|5          |1      |
|6    |Alta       |Gerenciamento de tarefas  |Eu, como usuário, quero poder adicionar, editar ou excluir tarefas de um projeto                            |8          |1      |
|1    |Alta       |Cadastro                  |Eu, como usuário, desejo visualizar métodos para realizar o cadastro utilizando um e-mail e senha           |3          |1      |
|2    |Alta       |Login                     |Eu, como usuário, desejo efetuar um login para poder acessar o sistema e verificar os projetos e tarefas vinculados a mim|3          |1      |
|4    |Alta       |Gerenciamento de equipes  |Eu, como usuário, desejo visualizar os demais membros, podendo editar, excluir ou acrescentar membros na equipe do projeto|5          |1      |
|5    |Alta       |Registro de tarefas       |Eu, como usuário, quero poder visualizar todas as tarefas de um projeto, vendo se elas estão pendentes, em desenvolvimento ou concluídas|13         |1      |

## User Story 1: Cadastro
**Eu, como usuário, desejo visualizar métodos para realizar o cadastro utilizando um e-mail e senha**

- O usuário deve conseguir se cadastrar selecionando a opção cadastrar e preenchendo os campos: Nome, Email e Senha

### Casos:
- **Caso 1:** O usuário inseriu um e-mail invalido
  - O sistema deve retornar um erro informando que o e-mail utilizado está inserido de forma incorreta
- **Caso 2:** O usuário inseriu um e-mail já cadastrado
  - O sistema deve retornar um erro informando que aquele e-mail já está sendo utilizado
- **Caso 3:** O usuário inseriu um e-mail não cadastrado
  - O sistema deve retornar um erro informando que não está cadastrado no sistema

---

## User Story 2: Login
**Eu, como usuário, desejo efetuar um login para poder acessar o sistema e verificar os projetos e tarefas vinculado a mim**

- O sistema deve verificar se E-mail e Senha inseridos são válidos para efetuar o login

### Casos:
- **Caso 1:** O usuário possui uma conta
  - O usuário entrará no sistema usando suas credenciais
- **Caso 2:** O usuário não possui uma conta
  - O usuário deve selecionar a opção de “cadastrar-se”

### Testes:
- **Teste 1:** O usuário digitou um e-mail inválido
  - O sistema deve retornar que o e-mail informado está incorreto
- **Teste 2:** O usuário digitou uma senha inválido
  - O sistema deve retornar que a senha informada está incorreta

---

## User Story 3: Gerenciamento de projetos
**Eu, como usuário, desejo visualizar todos os projetos que estão em aberto ou finalizados, podendo adicionar ou excluir projetos**

- O usuário deve conseguir criar, ver e excluir projetos, em caso de alteração o sistema deve mostrar um pop-up informado se foi excluido ou atualizado

### Casos:
- **Caso 1:** O projeto desejado ainda não existe
  - O usuário deve selecionar o botão novo projeto
- **Caso 2:** O sistema já possui o projeto desejado
  - O usuário pode selecioná-lo para ver mais sobre

---

## User Story 4: Gerenciamento de equipes
**Eu, como usuário, desejo visualizar os demais membros, excluir ou acrescentar membros na equipe do projeto**

- O usuário deve conseguir adicionar e excluir membros de um projeto, em caso de exclusão o sistema deve informar um pop-up informado a exclusão do membro

### Casos:
- **Caso 1:** O usuário deseja adicionar um novo membro ao projeto
  - O usuário seleciona um membro que deseja selecionar entre os cadastrados no sistema
- **Caso 2:** O usuário deseja excluir um membro do projeto
  - O usuário seleciona ao lado do nome do que deseja remover o botão “excluir”

---

## User Story 5: Registro de Tarefas
**Eu, como usuário, quero poder visualizar todas as tarefas de um projeto, vendo se elas estão pendentes, desenvolvimento ou concluídas**

- O usuário deve conseguir mover o card da tarefa entre as colunas de pendentes, desenvolvimento e concluídas, quando movidas o sistema deve atualizar seu status automaticamente
- O usuário deve conseguir selecionar uma tarefa e visualizar os seus detalhes, sendo eles: comentários, anexos, mudar status, descrição, titulo,prazo e responsáveis pela tarefa 

### Casos:
- **Caso 1:** O usuário seleciona um card de tarefa
  - O sistema deve abrir modal mostrando informações sobre aquela tarefa
- **Caso 2:** O usuário move um card de tarefa entre as colunas
  - O status daquela tarefa deve ser modificado para corresponder a coluna transferida

---

## User Story 6: Gerenciamento de Tarefas
**Eu, como usuário, quero poder adicionar, editar ou excluir tarefas de um projeto**

- O usuário deve conseguir criar novas tarefas, editar e excluir tarefas existentes
- O sistema deve permitir a adição de novos contribuintes em uma tarefa que já estejam cadastrados no projeto

### Casos:
- **Caso 1:** O usuário deseja adicionar uma nova tarefa
  - O usuário deve selecionar a opção “criar tarefa”, abrindo um modal de edição da mesma
- **Caso 2:** O usuário deseja editar os responsáveis da tarefa
  - Ele deve selecionar a tarefa e em “responsáveis” selecionar através de uma checkbox quais membros daquele projeto deve ser atribuídos a ela
- **Caso 3:** O usuário não deve ser capaz de colocar a data de uma tarefa posterior a data final do projeto
- **Caso 4:** O usuário não deve ser capaz de alterar o prazo da tarefa para uma data anterior a data atual