# 📋 SideQuest - Sistema de gerenciamento de tarefas

![Banner](./img/SideQuest.png)

# 🎯 Desafio

Em muitas equipes, o gerenciamento de tarefas ainda é feito de forma descentralizada, utilizando planilhas, anotações manuais ou ferramentas pouco integradas. Isso gera dificuldades em acompanhar prazos, priorizar atividades e manter uma comunicação clara entre os membros. Como resultado, há atrasos, retrabalho e perda de produtividade.

O desafio é oferecer uma solução que simplifique esse processo, permitindo que todos os integrantes da equipe tenham visibilidade sobre o andamento das tarefas, possam colaborar em tempo real e anexar documentos de suporte diretamente às atividades.

A SideQuest surge para resolver essas dores, proporcionando uma plataforma moderna, intuitiva e eficaz para organizar atividades, melhorar a comunicação interna e aumentar a eficiência do trabalho em equipe.

# 📝 Backlog do Produto

|Rank |Prioridade |Requisito                 |User Story                                                                                                  |Estimativa |Sprint |
|-----|-----------|--------------------------|------------------------------------------------------------------------------------------------------------|-----------|-------|
|1    |Alta       |Cadastro                  |Eu, como usuário, desejo visualizar métodos para realizar o cadastro utilizando um e--mail e senha           |5          |1      |
|2    |Alta       |Login                     |Eu, como usuário, desejo efetuar um login para poder acessar o sistema e verificar os projetos e tarefas vinculado a mim|5          |1      |
|3    |Alta       |Gerenciamento de projetos |Eu, como usuário, desejo visualizar todos os projetos que estão em aberto ou finalizados, podendo adicionar ou excluir projetos|5          |1      |
|4    |Alta       |Gerenciamento de equipes  |Eu, como usuário, desejo visualizar os demais membros, podendo editar, excluir ou acrescentar membros na equipe do projeto|5          |1      |
|5    |Alta       |Registro de tarefas       |Eu, como usuário, quero poder visualizar todas as tarefas de um projeto, vendo se elas estão pendentes, em desenvolvimento ou concluídas|13         |1      |
|6    |Alta       |Gerenciamento de tarefas  |Eu, como usuário, quero poder adicionar, editar ou excluir tarefas de um projeto                            |8          |1      |
|7    |Média      |Anexar arquivos           |Eu, como usuários, quero poder anexar arquivos a tarefas, em diferentes formatos                            |13         |2      |
|8    |Média      |Registro de entregas próximas|Eu, como sistema, quero informar ao usuário as tarefas com os prazos mais próximos                          |8          |2      |
|9    |Média      |Calendário do projeto     |Eu, como usuário, quero visualizar um calendário de entrega do projeto.                                     |34         |2      |
|12   |Média      |Tarefas por membros       |Eu, como sistema, desejo informar quantas tarefas foram concluídas por cada um dos membros de um projeto    |13         |2      |
|10   |Baixa      |Visualizar avisos         |Eu, como usuário, quero poder visualizar todas as notificações que foram ligadas ao meu usuário             |21         |3      |
|11   |Baixa      |Progresso do projeto      |Eu, como sistema, desejo informar o andamento do projeto.                                                   |21         |3      |
|13  |Baixa      |Lixeira                   |Eu, como sistema, devo armazenar todos os itens que forem excluídos em uma lixeira, permitindo sua exclusão completa ou restauração.                                      |21         |3      |


# 🗃️ Sprints 

| Sprint   | Periodo      | Status                |Documentação  | Link |
|----------|--------------|-----------------------|--------------|------| 
| Sprint 1 | 08/09 - 28/09| ✅ Concluida          |📄[Relatório](./docs/Sprint1/Sprint1.md)|🎥 [Vídeo](https://youtu.be/DhGwp1KHiGQ)| 
| Sprint 2 | 06/10 - 26/10| ✅ Concluida          |📄[Relatório](./docs/Sprint2/Sprint2.md)|🎥 [Vídeo](https://youtu.be/KwKw1hz7pbc)|
| Sprint 3 | 03/11 - 23/11| ⏳ Em andamento       |-------------|------|

# ⚙️ Tecnologias Utilizadas

![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)
![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Vite](https://img.shields.io/badge/vite-%23646CFF.svg?style=for-the-badge&logo=vite&logoColor=white)
![Apache Maven](https://img.shields.io/badge/Apache%20Maven-C71A36?style=for-the-badge&logo=Apache%20Maven&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-%234ea94b.svg?style=for-the-badge&logo=mongodb&logoColor=white)

# 📁 Estrutura do Projeto

## 🎨 **Frontend (SideQuest-FrontEnd)**

```
SideQuest-FrontEnd/
├── 📄 Configurações
│   ├── package.json           # Dependências e scripts npm
│   ├── vite.config.ts         # Configuração do Vite
│   ├── tailwind.config.js     # Configuração do Tailwind CSS
│   ├── eslint.config.js       # Regras de linting
│   └── tsconfig.*.json        # Configurações TypeScript
│
├── 📱 Aplicação Principal
│   ├── index.html             # HTML raiz
│   ├── src/
│   │   ├── main.tsx          # Ponto de entrada da aplicação
│   │   ├── App.tsx           # Componente raiz
│   │   ├── Layout.tsx        # Layout principal
│   │   └── index.css         # Estilos globais
│   │
│   ├── 📄 Páginas
│   │   ├── Acesso.tsx        # Página de login/cadastro
│   │   ├── Projetos.tsx      # Dashboard de projetos
│   │   ├── Membros.tsx       # Gerenciamento de membros
│   │   └── Tarefas.tsx       # Gestão de tarefas
│   │
│   ├── 🧩 Componentes
│   │   ├── Sidebar.tsx       # Menu lateral
│   │   ├── Modal.tsx         # Modal genérico
│   │   ├── CriarProjetoModal.tsx
│   │   ├── BotaoGoogle.tsx   # Autenticação Google
│   │   └── acesso/           # Componentes de autenticação
│   │       ├── PainelAcesso.tsx
│   │       ├── LoginForm.tsx
│   │       └── CadastroForm.tsx
│   │
│   ├── 🔧 Utilitários
│   │   ├── hooks/
│   │   │   └── useAuth.ts    # Hook de autenticação
│   │   ├── services/
│   │   │   └── ApiService.ts # Comunicação com backend
│   │   └── types/
│   │       └── api.ts        # Tipagens TypeScript
│   │
│   └── 🎨 Assets
│       └── assets/
```

## ⚙️ **Backend (SideQuest-BackEnd)**

```
SideQuest-BackEnd/
├── 📄 Configurações Maven
│   ├── pom.xml               # Dependências e configuração Maven
│   ├── mvnw / mvnw.cmd       # Maven Wrapper
│   └── .mvn/wrapper/
│
├── ☕ Código Java
│   └── src/main/java/com/syntax/sidequest_backend/
│       ├── 🚀 Aplicação Principal
│       │   └── SidequestBackendApplication.java
│       │
│       ├── 🌐 Controllers (API REST)
│       │   ├── UsuarioController.java
│       │   ├── ProjetoController.java
│       │   ├── TarefaController.java
│       │   └── MembroController.java
│       │
│       ├── 🏗️ Modelos
│       │   ├── entidade/          # Entidades JPA
│       │   └── dto/               # Data Transfer Objects
│       │
│       ├── 💾 Repositórios
│       │   ├── UsuarioRepositorio.java
│       │   ├── ProjetoRepositorio.java
│       │   ├── TarefaRepositorio.java
│       │   └── MembroRepositorio.java
│       │
│       ├── ⚙️ Serviços (Lógica de Negócio)
│       │   ├── UsuarioService.java
│       │   ├── ProjetoService.java
│       │   ├── TarefaService.java
│       │   └── MembroService.java
│       │
│       ├── 🛡️ Configurações
│       │   ├── configuracao/
│       │   │   └── CorsConfiguração.java
│       │   └── segurança/
│       │       └── SegurancaConfiguracao.java
│       │
│       └── ⚠️ Tratamento de Exceções
│           ├── ManipuladorGlobal.java
│           └── personalizado/
│
├── 📋 Recursos
│   └── src/main/resources/
│       ├── application.properties         # Configurações da aplicação
│       └── application.properties.example # Template de configuração
│
└── 🧪 Testes
    └── src/test/java/
        └── SidequestBackendApplicationTests.java
```

# 🚀 Como Executar

## 📋 **Pré-requisitos**

Certifique-se de ter instalado:
- ☕ **Java 17+** - Para executar o backend Spring Boot
- 📦 **Node.js 18+** - Para executar o frontend React
- 🔧 **Maven** - Gerenciador de dependências Java (ou use o wrapper incluído)
- 💾 **Git** - Para clonar o repositório

## 📥 **1. Clone o Repositório**

```bash
git clone https://github.com/Syntax-Fatec-SJC/SideQuest.git
cd SideQuest
```

## ⚙️ **2. Configuração e Execução do Backend**

### **Navegue para o diretório do backend:**
```bash
cd SideQuest-BackEnd/sidequest-backend
```

### **Configure o banco de dados:**
1. Copie o arquivo de exemplo:
   ```bash
   cp src/main/resources/application.properties.example src/main/resources/application.properties
   ```

2. Edite o `application.properties` com suas configurações de banco de dados

### **Execute o backend:**

**Opção 1: Usando Maven Wrapper (Recomendado)**
```bash
# Windows
./mvnw.cmd spring-boot:run

# Linux/Mac
./mvnw spring-boot:run
```

**Opção 2: Usando Maven instalado**
```bash
mvn spring-boot:run
```

### **Verificação:**
- ✅ O backend estará rodando em: `http://localhost:8080`
- 🔍 Health check: `http://localhost:8080/actuator/health`

## 🎨 **3. Configuração e Execução do Frontend**

### **Abra um novo terminal** e navegue para o diretório do frontend:
```bash
cd SideQuest-FrontEnd/SideQuest-FrontEnd
```

### **Instale as dependências:**
```bash
npm install
```

### **Execute o frontend:**

**Modo de desenvolvimento:**
```bash
npm run dev
```

**Build para produção:**
```bash
npm run build
npm run preview
```

### **Verificação:**
- ✅ O frontend estará rodando em: `http://localhost:5173`
- 🌐 Acesse no navegador para ver a aplicação

## 🔧 **4. Scripts Disponíveis**

### **Backend (Maven)**
- `./mvnw spring-boot:run` - Executa a aplicação
- `./mvnw test` - Executa os testes
- `./mvnw clean compile` - Limpa e compila o projeto
- `./mvnw package` - Gera o arquivo JAR

### **Frontend (npm)**
- `npm run dev` - Modo desenvolvimento com hot reload
- `npm run build` - Build para produção
- `npm run preview` - Preview do build de produção
- `npm run lint` - Executa o linting do código


## 🔍 **6. Verificação da Comunicação**

1. **Backend ativo:** `http://localhost:8080`
2. **Frontend ativo:** `http://localhost:5173`
3. **API endpoints:** `http://localhost:8080/api/*`

### **Teste a comunicação:**
- Acesse o frontend e tente fazer login
- Verifique no Network do navegador se as chamadas API estão funcionando
- Console do backend deve mostrar as requisições recebidas

## ⚠️ **Troubleshooting**

### **Problemas Comuns:**

**Backend não inicia:**
- Verifique se o Java 17+ está instalado: `java -version`
- Confirme se a porta 8080 não está em uso
- Verifique as configurações do banco de dados

**Frontend não inicia:**
- Verifique se o Node.js está instalado: `node -version`
- Limpe o cache: `npm cache clean --force`
- Delete node_modules e reinstale: `rm -rf node_modules && npm install`

# Documentação
- 📄 [Documentação](./docs)
- 📄 [Sprint-1](./docs/Sprint1/)
- 📄 [Sprint-2](./docs/Sprint2/)
- 📄 [Sprint-3](./docs/Sprint3/)
- 📄 [EndPoints](http://localhost:8080/swagger-ui/index.html) 
    - Para testar os endpoints primeiro inicie o backend do projeto


# 👨‍💻 Equipe de Desenvolvimento

| Foto                                                                          | Função        | Nome              | GitHub                                         | LinkedIn                                                              |
|-------------------------------------------------------------------------------|---------------|-------------------|------------------------------------------------|-----------------------------------------------------------------------|
| <img src="https://avatars.githubusercontent.com/LucasAraujo1016" width=50px>  | Scrum Master  | Lucas Araujo      | [![GitHub Badge](https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white)](https://github.com/LucasAraujo1016)   | [![Linkedin Badge](https://img.shields.io/badge/Linkedin-blue?style=flat-square&logo=Linkedin&logoColor=white)](https://www.linkedin.com/in/lucas-araujo-448115329)        |
| <img src="https://avatars.githubusercontent.com/LittleRob120" width=50px>     | Product Owner | Gabriel Robert    | [![GitHub Badge](https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white)](https://github.com/LittleRob120)      | [![Linkedin Badge](https://img.shields.io/badge/Linkedin-blue?style=flat-square&logo=Linkedin&logoColor=white)](https://www.linkedin.com/in/gabriel-robert-123ba7258)      |
| <img src="https://avatars.githubusercontent.com/TatianeOliveira8" width=50px> | Dev Team      | Tatiane Olivera   | [![GitHub Badge](https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white)](https://github.com/TatianeOliveira8)  | [![Linkedin Badge](https://img.shields.io/badge/Linkedin-blue?style=flat-square&logo=Linkedin&logoColor=white)](https://www.linkedin.com/in/tatiane-oliveira-332155377)    |
| <img src="https://avatars.githubusercontent.com/joaovvsilva" width=50px>      | Dev Team      | João Silva        | [![GitHub Badge](https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white)](https://github.com/joaovvsilva)       | [![Linkedin Badge](https://img.shields.io/badge/Linkedin-blue?style=flat-square&logo=Linkedin&logoColor=white)](https://www.linkedin.com/in/jo%C3%A3o-vitor-ven%C3%A2ncio-da-silva-b0239819b/) |
| <img src="https://media.licdn.com/dms/image/v2/D4D03AQG3F8_tpuj3-A/profile-displayphoto-shrink_400_400/B4DZXoEeWUHAAg-/0/1743355242312?e=1762992000&v=beta&t=ADZDXokbUQiyVIouF3OpgDBakoRitnACJYpiklTwizY" width=50px>     | Dev Team      | Francisco Rafael  | [![GitHub Badge](https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white)](https://github.com/franciscorafaelpires) | [![Linkedin Badge](https://img.shields.io/badge/Linkedin-blue?style=flat-square&logo=Linkedin&logoColor=white)](https://www.linkedin.com/in/francisco-rafael-pires-755958163/) |
| <img src="https://avatars.githubusercontent.com/carlosintrieri" width=50px>   | Dev Team      | Carlos Intrieri   | [![GitHub Badge](https://img.shields.io/badge/GitHub-111217?style=flat-square&logo=github&logoColor=white)](github.com/carlosintrieri)            | [![Linkedin Badge](https://img.shields.io/badge/Linkedin-blue?style=flat-square&logo=Linkedin&logoColor=white)](linkedIn.com/in/carlosintrieri)                            |
