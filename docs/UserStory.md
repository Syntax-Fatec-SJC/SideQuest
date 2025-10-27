# Critérios de aceitação

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

---

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

## User Story 10: Visualizar avisos
**Eu, como usuário, quero poder visualizar todas as notificações que foram ligadas ao meu usuário** 

- O usuário deve possuir uma página com todos os avisos referentes a ele
- O usuário deve poder visualizar gráficos mostrando quais tarefas estão: pendentes, em desenvolvimento e concluída
- O usuário deve poder visualizar os avisos na página de dashboard, os avisos no presentes no dashboard devem apresentar o título, uma pequena parte da mensagem e a data do aviso
- Os avisos devem possuir uma data de envio tanto na página de dashboard quanto na página de avisos

### Casos:
- **Caso 1:** Uma nova tarefa é atribuída ao usuário
  - O sistema informa ao usuário que uma nova tarefa foi atribuída a ele
- **Caso 2:** Uma tarefa é excluída 
  - O sistema informar os usuários atribuídos a tarefa sobre sua exclusão
- **Caso 3:** Um projeto é excluído
  - O sistema informa os usuários atribuídos ao projeto sobre sua exclusão
- **Caso 4:** Uma tarefa é editada
  - O sistema informa os usuários atribuído a tarefa sobre a sua edição
  - O sistema deve notificar todos os membros envolvidos na tarefa caso haja alguma modificação

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
**Eu, como sistema, deve salvar todos os arquivos excluídos por um período de tempo antes da exclusão definitiva desse arquivo**

- O sistema deve armazenar o último estado do arquivo na página de “Lixeira”
- O sistema deve retornar o arquivo para o mesmo estado que estava antes da exclusão

### Casos:
- **Caso 1:** Uma tarefa foi excluída
  - O sistema deve armazenar o status da tarefa e os membros responsáveis pela tarefa
- **Caso 2:** Uma tarefa foi restaurada
  - O sistema deve retornar a tarefa para o mesmo local de status junto com os responsáveis pela mesma
- **Caso 3:** Um projeto foi excluído
  - O sistema deve armazenar todos os estados, membros, imagens e tarefas ligadas ao projeto
- **Caso 4:** Um projeto foi restaurado
  - O sistema deve retornar o projeto para o mesmo status, progresso e os arquivos

