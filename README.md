📋 Funcionalidades
✅ Busca em pastas do OneDrive compartilhadas via link público

✅ Suporte para links no formato https://onedrive.live.com/?id=...&redeem=...

✅ Resultados exibidos com links diretos para os arquivos

🛠️ Tecnologias Utilizadas
Frontend: React.js

Backend: Node.js

API: Microsoft Graph API

Autenticação: OAuth 2.0 (Client Credentials)

📋 Pré-requisitos
Node.js (v14 ou superior)

NPM ou Yarn

Uma conta Microsoft Azure com acesso para criar App Registrations

O link público da pasta do OneDrive

🚀 Configuração do Azure (Passo a Passo)
1. Criar um App Registration no Azure
Acesse Azure Portal

Navegue para Azure Active Directory → App registrations

Clique em + New registration

Preencha:

Name: OneDrive Search App

Supported account types: Accounts in this organizational directory only

Redirect URI: http://localhost:3000 (para desenvolvimento)

Clique em Register

2. Obter Credenciais
Após o registro, anote:

Application (client) ID → será seu CLIENT_ID

Directory (tenant) ID → será seu TENANT_ID

3. Gerar Client Secret
No menu do app, clique em Certificates & secrets

Clique em + New client secret

Preencha:

Description: Secret para desenvolvimento

Expires: 24 months (ou conforme necessidade)

Clique em Add

Copie o valor imediatamente → será seu CLIENT_SECRET

4. Configurar Permissões
No menu do app, clique em API permissions

Clique em + Add a permission

Selecione Microsoft Graph → Application permissions

Busque e marque Files.Read.All

Clique em Add permissions

Clique em Grant admin consent (botão no topo)

Confirme clicando em Yes



# server
mkdir server
cd server
npm init -y
npm install express cors multer @azure/msal-node axios dotenv
npm install -D nodemon

# client
npx create-react-app client
cd client
npm install axios


# 1. Inicializa o repositório Git na pasta do seu projeto
git init

# 2. Adiciona todos os arquivos do projeto para a "área de preparação"
git add .

# 3. Cria o primeiro commit com uma mensagem descritiva
git commit -m "Commit inicial do projeto"

# 4. Renomeia a branch principal para 'main' (padrão atual do GitHub)
git branch -M main

# 5. Conecta seu repositório local ao remoto no GitHub
git remote add origin https://github.com/anaandrades08/onedrive-search.git

# 6. Envia (push) seu código para o GitHub
git push -u origin main