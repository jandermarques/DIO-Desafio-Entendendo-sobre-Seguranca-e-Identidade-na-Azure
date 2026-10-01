# ☁️ README - Microsoft Entra ID e Segurança no Azure

## 📖 Introdução
O **Microsoft Entra ID** (antigo Azure Active Directory) é o serviço de identidade e acesso da Microsoft. Ele garante autenticação, autorização e gerenciamento de usuários, grupos e aplicações, tanto em ambientes **cloud** quanto **on-premises**.

---

## 1️⃣ Microsoft Entra ID

### 🔹 Users
- Representam contas individuais (funcionários, parceiros, convidados).
- Podem ser criados manualmente ou sincronizados via **Entra Connect**.

### 🔹 Groups
- Conjunto de usuários com permissões e políticas comuns.
- Simplificam a atribuição de acesso a recursos.

### 🔹 External Identities
- Permitem convidar usuários externos (parceiros, fornecedores) para acessar recursos da organização.
- Usam autenticação federada ou contas Microsoft pessoais.

### 🔹 Roles e Administrators
- **Roles**: definem permissões (ex.: Global Administrator, User Administrator).
- **Administrators**: usuários atribuídos a roles específicas para gerenciar recursos.

### 🔹 Enterprise Applications
- Aplicações integradas ao Entra ID para autenticação via **Single Sign-On (SSO)**.
- Ex.: Salesforce, ServiceNow, Office 365.

---

## 2️⃣ Logs e Saúde

- **Audit Logs**: registram alterações administrativas (criação de usuários, atribuição de roles).
- **Sign-in Logs**: mostram tentativas de login, sucesso ou falha, incluindo localização e dispositivo.
- **Health**: painel de status do serviço, notificações de incidentes e recomendações.

---

## 3️⃣ Deleção e Restauração de Users
- Usuários deletados ficam em estado de **soft delete** por até **30 dias**.
- Podem ser restaurados pelo portal ou via PowerShell.
- Após 30 dias, a exclusão é permanente.

---

## 4️⃣ Self-Service Password Reset (SSPR)
- Permite que usuários redefinam suas senhas sem intervenção do administrador.
- Usa métodos de verificação como SMS, e-mail alternativo ou aplicativo autenticador.
- Reduz carga do helpdesk e aumenta segurança.

---

## 5️⃣ Microsoft Entra Connect
- Ferramenta que sincroniza identidades do **Active Directory local** com o **Entra ID**.
- Permite login único (SSO) e mantém consistência entre ambientes híbridos.

---

## 6️⃣ Microsoft Defender for Cloud
- Serviço de monitoramento e proteção contra ameaças em ambientes **Azure** e **on-premises**.
- Oferece recomendações de segurança, proteção de workloads e conformidade regulatória.
- Integra-se com Entra ID para reforçar políticas de acesso.

---

## ⚙️ Passo a Passo - Criando e Gerenciando Usuários no Portal Azure

### 1. Criar um Usuário
- Acesse [portal.azure.com](https://portal.azure.com).
- Vá em **Microsoft Entra ID** → **Usuários** → **+ Novo Usuário**.
- Preencha:
  - Nome.
  - Nome de usuário (login).
  - Senha inicial.
- Clique em **Criar**.

### 2. Convidar Usuário Externo
- Em **Microsoft Entra ID** → **Usuários** → **+ Novo Usuário Externo**.
- Escolha **Convidar usuário**.
- Informe o e-mail do convidado.
- Defina grupo ou role (opcional).
- Clique em **Convidar** (o usuário receberá e-mail de convite).

### 3. Criar Grupo e Adicionar Usuários
- Em **Microsoft Entra ID** → **Grupos** → **+ Novo Grupo**.
- Defina:
  - Tipo de grupo (Segurança ou Microsoft 365).
  - Nome do grupo.
- Adicione usuários internos ou externos.
- Clique em **Criar**.

### 4. Atribuir Role a Usuário ou Grupo
- Em **Microsoft Entra ID** → **Funções e Administradores**.
- Selecione a role desejada (ex.: User Administrator).
- Clique em **+ Atribuir**.
- Escolha o usuário ou grupo.
- Clique em **Adicionar**.

---

## ✅ Conclusão
O **Microsoft Entra ID** é a espinha dorsal da identidade no Azure, garantindo segurança e governança. Com recursos como **Users, Groups, Roles, Enterprise Applications, SSPR e Entra Connect**, é possível gerenciar acessos de forma eficiente. Integrado ao **Microsoft Defender for Cloud**, fortalece a defesa contra ameaças em ambientes híbridos.

