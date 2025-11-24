## 📥 **1. Clone o Repositório**

```bash
git clone https://github.com/Syntax-Fatec-SJC/SideQuest.git
cd SideQuest
```

## ⚙️ **2. Configuração e Execução do Backend (Microserviços)**

O backend é composto por múltiplos microserviços. Cada um precisa ser executado em seu próprio terminal.

### **Para cada serviço abaixo (`api-gateway`, `usuario-service`, etc.):**

1.  **Abra um novo terminal** para cada serviço.
2.  **Navegue até o diretório do serviço**. Exemplo para o `usuario-service`:
    ```bash
    cd SideQuest-BackEnd/usuario-service
    ```
3.  **(Opcional) Configure o banco de dados:** Se for o primeiro uso, edite o arquivo `src/main/resources/application.properties` com as credenciais do seu banco de dados.
4.  **Execute o serviço** usando o Maven Wrapper:
    ```bash
    # Windows
    ./mvnw.cmd spring-boot:run

    # Linux/Mac
    ./mvnw spring-boot:run
    ```

### **Serviços a serem executados:**
Você deve iniciar os seguintes serviços, cada um em seu próprio terminal:
- `api-gateway`
- `usuario-service`
- `projetos-service`
- `tarefas-service`
- `avisos-service`
- `anexo-service`

### **Verificação:**
- ✅ O **API Gateway** (ponto de entrada) estará rodando em: `http://localhost:8080` (ou a porta configurada).
- ✅ Os outros serviços estarão rodando em suas respectivas portas, conforme configurado no `application.properties` de cada um.

## 🎨 **3. Configuração e Execução do Frontend**

### **Abra um novo terminal** e navegue para o diretório do frontend:
```bash
cd SideQuest-FrontEnd
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

### **Verificação:**
- ✅ O frontend estará rodando em: `http://localhost:5173`
- 🌐 Acesse este endereço no navegador para ver a aplicação.

## 🔧 **4. Scripts Disponíveis**

### **Backend (Maven - em cada diretório de microserviço)**
- `./mvnw spring-boot:run` - Executa a aplicação
- `./mvnw test` - Executa os testes
- `./mvnw clean package` - Limpa, compila e gera o arquivo JAR

### **Frontend (npm)**
- `npm run dev` - Modo desenvolvimento com hot reload
- `npm run build` - Build para produção
- `npm run preview` - Preview do build de produção
- `npm run lint` - Executa o linting do código


## 🔍 **6. Verificação da Comunicação**

1. **Backend ativo:** Certifique-se de que todos os microserviços e o API Gateway estão rodando.
2. **Frontend ativo:** `http://localhost:5173`
3. **API endpoints via Gateway:** `http://localhost:8080/`

### **Teste a comunicação:**
- Acesse o frontend e tente fazer login ou se cadastrar.
- Verifique no painel "Rede" (Network) do navegador se as chamadas para `http://localhost:8080/...` estão funcionando.
- O console do terminal de cada microserviço deve mostrar as requisições recebidas.

## ⚠️ **Troubleshooting**

### **Problemas Comuns:**

**Microserviço não inicia:**
- Verifique se o Java 17+ está instalado: `java -version`
- Confirme se a porta configurada para o serviço não está em uso por outro processo.
- Verifique as configurações no `application.properties` (banco de dados, portas, etc.).

**Frontend não inicia:**
- Verifique se o Node.js está instalado: `node -version`
- Limpe o cache: `npm cache clean --force`
- Delete a pasta `node_modules` e o arquivo `package-lock.json`, e reinstale: `rm -rf node_modules package-lock.json && npm install`