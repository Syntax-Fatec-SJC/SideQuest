## 🎨 **Frontend (SideQuest-FrontEnd)**

A estrutura do frontend foi organizada utilizando uma abordagem de **Feature-Sliced Design**, onde cada funcionalidade principal da aplicação (como `auth`, `projetos`, `tarefas`) possui seu próprio diretório contendo seus componentes, hooks e lógica específicos.

```
SideQuest-FrontEnd/
├── 📄 Configurações
│   ├── package.json           # Dependências e scripts npm
│   ├── vite.config.ts         # Configuração do Vite
│   ├── tailwind.config.js     # Configuração do Tailwind CSS
│   ├── eslint.config.js       # Regras de linting
│   └── tsconfig.*.json        # Configurações TypeScript
│
├── 📱 Aplicação Principal (src/)
│   ├── main.tsx               # Ponto de entrada da aplicação
│   ├── App.tsx                # Componente raiz com rotas
│   ├── Layout.tsx             # Layout principal (com Sidebar)
│   └── index.css              # Estilos globais
│
├── ✨ Features (src/features/)
│   ├── auth/                  # Autenticação
│   │   ├── Acesso.tsx
│   │   ├── components/
│   │   ├── hooks/
│   │   └── ...
│   ├── projetos/              # Gestão de Projetos
│   ├── tarefas/               # Gestão de Tarefas
│   ├── membros/               # Gestão de Membros
│   ├── avisos/                # Mural de Avisos
│   ├── calendario/            # Calendário de Entregas
│   ├── dashboard/             # Dashboard principal
│   └── ...                    # Outras features
│
├── 📦 Compartilhado (src/shared/)
│   ├── components/            # Componentes reutilizáveis (Sidebar, ProtecaoPage)
│   ├── contexts/              # Contextos globais (ToastContext)
│   ├── errors/                # Tratamento de erros
│   ├── hooks/                 # Hooks globais (useAuth, useToast)
│   └── types/                 # Tipagens compartilhadas
│
├── 📞 Serviços (src/services/)
│   ├── ApiBase.ts             # Configuração base do Axios
│   ├── AuthService.ts         # Serviço de autenticação
│   ├── ProjetoService.ts      # Serviço de projetos
│   ├── TarefaService.ts       # Serviço de tarefas
│   └── ...                    # Outros serviços
│
├── 📝 Tipos (src/types/)
│   ├── Projeto.ts             # Tipagens de domínio para Projeto
│   ├── Tarefa.ts              # Tipagens de domínio para Tarefa
│   └── ...                    # Outras tipagens de domínio
│
└── 🎨 Assets (src/assets/)
    └── ...                    # Imagens, ícones, etc.
```

## ⚙️ **Backend (Microserviços)**

O backend foi reestruturado para uma arquitetura de **microserviços**, onde cada domínio de negócio é uma aplicação Spring Boot independente, comunicando-se através de um API Gateway.

```
SideQuest-BackEnd/
├── 🚪 api-gateway/            # Ponto de entrada único para o frontend
│
├── 👤 usuario-service/        # Gerencia usuários e autenticação
├── 🏗️ projetos-service/       # Gerencia projetos e membros
├── ✅ tarefas-service/        # Gerencia tarefas e subtarefas
├── 📢 avisos-service/         # Gerencia o mural de avisos
├── 📎 anexo-service/          # Gerencia o upload e armazenamento de anexos
└── ...                        # Outros microserviços
```

### Estrutura de um Microserviço (Ex: `usuario-service`)

```
usuario-service/
├── 📄 pom.xml                 # Dependências e configuração Maven
│
├── ☕ Código Java (src/main/java/com/syntax/...)
│   ├── 🚀 Application.java    # Ponto de entrada do serviço
│   ├── 🌐 controller/         # Endpoints da API REST
│   ├── 📦 model/              # Entidades e DTOs
│   ├── 💾 repository/         # Acesso ao banco de dados (JPA)
│   ├── ⚙️ service/            # Lógica de negócio
│   └── 🛡️ config/            # Configurações (Segurança, CORS)
│
├── 📋 Recursos (src/main/resources/)
│   └── application.properties # Configurações (banco de dados, porta, etc.)
│
└── 🧪 Testes (src/test/java/...)
```