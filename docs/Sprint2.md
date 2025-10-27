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

## Definition of Ready (DoR)

Os critérios abaixo representam o que precisa estar preparado antes do desenvolvimento:

- **Calendário funcional** — Especificações definidas para exibir e gerenciar tarefas e eventos.
- **Conseguir anexar arquivos nas tarefas** — Tipos de arquivo e tamanho máximo definidos.
- **Registro de membros funcional** — Campos obrigatórios, regras de validação e fluxos de cadastro estabelecidos.
- **Gráficos das tarefas ligadas ao usuário** — Fontes de dados e formato dos gráficos definidos.
- **Validação de erros** — Regras e mensagens de erro documentadas.

## Definition of Done (DoD)

Os critérios abaixo definem quando cada item do DoR está considerado concluído e pronto para entrega:

- **Calendário funcional**
    - ✅ Exibe corretamente todas as tarefas e eventos vinculados ao usuário.
    - ✅ Permite adicionar, editar e remover tarefas.
    - ✅ Atualiza automaticamente as alterações (sem recarregar a página, se aplicável).
    - ✅ Interface responsiva e validada em navegadores principais.
- **Anexar arquivos nas tarefas**
    - ❌ O usuário pode anexar um ou mais arquivos às tarefas.
    - ❌ Tipos e tamanhos de arquivo são validados conforme o especificado.
    - ❌ Os arquivos são armazenados com segurança (ex: no servidor ou serviço em nuvem).
    - ❌ Exibição e download dos anexos funcionando corretamente.
- **Registro de membros funcional**
    - ✅ Fluxo de cadastro e login implementado e testado.
    - ✅ Dados persistem corretamente no banco.
    - ✅ Mensagens de validação e erro claras.
    - ✅ Validação de duplicidade (ex: e-mail já cadastrado).
    - ✅ Testes manuais e/ou automatizados comprovam o funcionamento.
- **Gráficos das tarefas ligadas ao usuário**
    - ✅ Os gráficos exibem corretamente as tarefas atribuídas ao usuário.
    - ✅ Atualizam conforme newStringos dados são adicionados ou alterados.
    - ✅ Design segue o padrão visual do sistema.
    - ✅ Dados e legendas exibidos de forma clara e legível.
- **Validação de erros**
    - ❌ Todas as ações do usuário possuem mensagens de erro claras e úteis.
    - ❌ Erros são tratados tanto no front quanto no back-end.
    - ❌ Nenhum erro não tratado aparece no console.
    - ❌ Logs de erros relevantes são registrados (quando aplicável). 
