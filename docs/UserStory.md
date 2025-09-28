# Critérios de Aceitação

## User Story 1: Cadastro
**Eu, como usuário, desejo visualizar métodos para realizar o cadastro utilizando um e-mail e senha.**

- O usuário deve conseguir se cadastrar selecionando a opção "Cadastrar" e preenchendo os campos: Nome, Email e Senha.

### Casos:
- **Caso 1:** O usuário inseriu um e-mail inválido  
  - O sistema deve retornar um erro informando que o e-mail está incorreto.  
- **Caso 2:** O usuário inseriu um e-mail já cadastrado  
  - O sistema deve retornar um erro informando que o e-mail já está em uso.  
- **Caso 3:** O usuário inseriu um e-mail não cadastrado  
  - O sistema deve retornar um erro informando que o e-mail não está cadastrado.

---

## User Story 2: Login
**Eu, como usuário, desejo efetuar um login para acessar o sistema e verificar os projetos e tarefas vinculados a mim.**

- O sistema deve verificar se E-mail e Senha inseridos são válidos.

### Casos:
- **Caso 1:** O usuário possui uma conta  
  - Entrará no sistema usando suas credenciais.  
- **Caso 2:** O usuário não possui uma conta  
  - Deve selecionar a opção “Cadastrar-se”.

### Testes:
- **Teste 1:** Usuário digitou e-mail inválido  
  - O sistema deve retornar que o e-mail informado está incorreto.  
- **Teste 2:** Usuário digitou senha inválida  
  - O sistema deve retornar que a senha informada está incorreta.

---

## User Story 3: Gerenciamento de projetos
**Eu, como usuário, desejo visualizar todos os projetos que estão em aberto ou finalizados, podendo adicionar ou excluir projetos.**

- O usuário deve conseguir criar, ver e excluir projetos.

### Casos:
- **Caso 1:** O projeto desejado ainda não existe  
  - Usuário deve selecionar o botão "Novo Projeto".  
- **Caso 2:** O sistema já possui o projeto desejado  
  - Usuário pode selecioná-lo para ver mais detalhes.

---

## User Story 4: Gerenciamento de equipes
**Eu, como usuário, desejo visualizar os demais membros, excluir ou acrescentar membros na equipe do projeto.**

- O usuário deve conseguir adicionar e excluir membros de um projeto.

### Casos:
- **Caso 1:** Adicionar novo membro ao projeto  
  - Usuário seleciona um membro entre os cadastrados no sistema.  
- **Caso 2:** Excluir um membro do projeto  
  - Usuário clica no botão “Excluir” ao lado do membro que deseja remover.

---

## User Story 5: Registro de Tarefas
**Eu, como usuário, quero poder visualizar todas as tarefas de um projeto, vendo se estão pendentes, em desenvolvimento ou concluídas.**

- O usuário deve conseguir mover o card da tarefa entre as colunas: Pendentes, Desenvolvimento e Concluídas.  
- O usuário deve conseguir selecionar uma tarefa e visualizar seus detalhes.

### Casos:
- **Caso 1:** Seleciona um card de tarefa  
  - Sistema abre modal mostrando informações da tarefa.  
- **Caso 2:** Move um card de tarefa entre colunas  
  - Status da tarefa é atualizado para corresponder à coluna transferida.

---

## User Story 6: Gerenciamento de Tarefas
**Eu, como usuário, quero poder adicionar, editar ou excluir tarefas de um projeto.**

- O usuário deve conseguir criar, editar e excluir tarefas existentes.  
- O sistema deve permitir adicionar novos responsáveis a uma tarefa.

### Casos:
- **Caso 1:** Adicionar nova tarefa  
  - Usuário seleciona “Criar Tarefa” e abre modal de edição.  
- **Caso 2:** Editar responsáveis da tarefa  
  - Seleciona a tarefa e define os responsáveis via checkbox.

---

## User Story 7: Anexo de Arquivos
**Eu, como usuário, quero anexar arquivos a tarefas em diferentes formatos.**

- Formatos permitidos: PDF, PNG, JPEG, DOCX, MP4.  
- Para concluir a tarefa, pelo menos um arquivo deve ser anexado.  
- Usuário consegue visualizar todos os arquivos anexados.

### Casos:
- **Caso 1:** Arquivo válido anexado  
  - Tarefa pode ser concluída.  
- **Caso 2:** Nenhum arquivo anexado  
  - Sistema impede conclusão e informa que pelo menos um arquivo deve ser anexado.

### Testes:
- **Teste 1:** Arquivo em formato inválido  
  - Sistema rejeita o arquivo e informa formatos válidos.

---

## User Story 8: Registro de próximas entregas
**Eu, como usuário, quero visualizar as tarefas atribuídas a mim com os prazos mais próximos.**

- Página própria mostrando tarefas com prazos próximos.  
- Ao selecionar uma tarefa, usuário é direcionado para o projeto correspondente.

### Casos:
- **Caso 1:** Tarefa próxima da entrega  
  - Usuário visualiza que o prazo está próximo.  
- **Caso 2:** Seleciona uma tarefa  
  - Usuário é redirecionado para a página do projeto correspondente.

---

## User Story 9: Calendário
**Eu, como usuário, quero visualizar um calendário de entregas do projeto.**

- Calendário geral do projeto e calendário pessoal do usuário.  
- Usuário pode alternar entre os dois.

### Casos:
- **Caso 1:** Nova tarefa criada  
  - Adiciona tarefa no calendário do projeto.  
- **Caso 2:** Tarefa atribuída a um usuário  
  - Adiciona tarefa no calendário pessoal do usuário.  
- **Caso 3:** Seleção do calendário  
  - Sistema alterna entre calendário do projeto e pessoal.

---

## User Story 10: Visualizar avisos
**Eu, como usuário, quero visualizar todas as notificações ligadas ao meu usuário.**

- Página com todos os avisos do usuário.

### Casos:
- **Caso 1:** Nova tarefa atribuída  
  - Sistema notifica o usuário.  
- **Caso 2:** Tarefa excluída  
  - Sistema notifica usuários atribuídos à tarefa.  
- **Caso 3:** Projeto excluído  
  - Sistema notifica usuários envolvidos.  
- **Caso 4:** Tarefa editada  
  - Sistema notifica todos os membros da tarefa sobre a edição.

---

## User Story 11: Progresso do projeto
**Eu, como usuário, desejo visualizar o progresso total de um projeto.**

- Barra de progresso mostrando % concluída baseada em número de tarefas.  
- Gráfico de pizza mostrando status das tarefas: Pendente, Em Desenvolvimento, Concluídas e Atrasadas.

### Casos:
- **Caso 1:** Nova tarefa adicionada  
  - Adiciona tarefa ao gráfico como “Pendente”.  
- **Caso 2:** Tarefa entra em desenvolvimento  
  - Atualiza status no gráfico para “Em Desenvolvimento”.  
- **Caso 3:** Tarefa atrasada  
  - Atualiza status para “Atraso”.  
- **Caso 4:** Tarefa concluída  
  - Atualiza status para “Concluído” e aumenta barra de progresso.  
- **Caso 5:** Tarefa removida  
  - Atualiza gráfico e barra de progresso de acordo.

---

## User Story 12: Tarefas por membros
**Eu, como sistema, desejo informar quantas tarefas foram concluídas por cada membro de um projeto.**

- Gráfico de barras mostrando quantidade de tarefas por membro, destacando quem possui mais tarefas.

### Casos:
- **Caso 1:** Tarefa atribuída a um membro  
  - Atualiza contagem de tarefas do usuário.  
- **Caso 2:** Tarefa removida  
  - Atualiza contagem de tarefas do usuário.  
- **Caso 3:** Novo usuário com mais tarefas que outros  
  - Atualiza gráfico para mostrar o usuário com mais tarefas.
