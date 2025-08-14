# 📚 Como Subir o Iluminavoz para o GitHub - Passo a Passo

## 🎯 **Pré-requisitos**
- Ter uma conta no GitHub (gratuita)
- Git instalado no computador

---

## 📝 **Passo 1: Criar Conta no GitHub**

1. **Acesse:** https://github.com
2. **Clique em:** "Sign up" (Cadastrar-se)
3. **Preencha:**
   - Username (nome de usuário único)
   - Email
   - Senha
4. **Confirme** o email recebido
5. **Pronto!** Sua conta está criada

---

## 🗂️ **Passo 2: Criar Repositório no GitHub**

1. **Faça login** no GitHub
2. **Clique no "+"** no canto superior direito
3. **Selecione:** "New repository"
4. **Preencha:**
   - Repository name: `iluminavoz`
   - Description: `App de Fonoaudiologia - Portal do Paciente`
   - ✅ Public (para deploy gratuito)
   - ❌ NÃO marque "Add a README file"
5. **Clique:** "Create repository"

---

## 💻 **Passo 3: Preparar o Código Local**

No terminal, dentro da pasta do projeto Iluminavoz:

```bash
# 1. Inicializar Git (se ainda não foi feito)
git init

# 2. Adicionar todos os arquivos
git add .

# 3. Fazer o primeiro commit
git commit -m "Iluminavoz - App de Fonoaudiologia completo"

# 4. Renomear branch para main
git branch -M main
```

---

## 🔗 **Passo 4: Conectar com GitHub**

```bash
# Substitua SEU_USUARIO pelo seu nome de usuário do GitHub
git remote add origin https://github.com/SEU_USUARIO/iluminavoz.git

# Exemplo: se seu usuário for "maria123":
# git remote add origin https://github.com/maria123/iluminavoz.git
```

---

## ⬆️ **Passo 5: Enviar Código para GitHub**

```bash
# Enviar código para o GitHub
git push -u origin main
```

**Se pedir login:**
- Username: seu nome de usuário do GitHub
- Password: use um **Personal Access Token** (não a senha normal)

### 🔑 **Como criar Personal Access Token:**
1. GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)
2. "Generate new token (classic)"
3. Marque: `repo` (acesso completo aos repositórios)
4. Copie o token gerado (guarde bem!)
5. Use este token como senha

---

## ✅ **Passo 6: Verificar se Funcionou**

1. **Acesse:** https://github.com/SEU_USUARIO/iluminavoz
2. **Você deve ver** todos os arquivos do projeto
3. **Pronto!** Código está no GitHub

---

## 🚀 **Passo 7: Deploy na Vercel (Opcional)**

Agora que está no GitHub, pode fazer deploy:

1. **Acesse:** https://vercel.com
2. **Login com GitHub**
3. **"New Project"**
4. **Selecione:** repositório "iluminavoz"
5. **Deploy** (automático!)
6. **Receba a URL:** `https://iluminavoz-xxx.vercel.app`

---

## 🔄 **Para Futuras Atualizações**

Quando fizer mudanças no código:

```bash
# 1. Adicionar mudanças
git add .

# 2. Commit com descrição
git commit -m "Descrição da mudança"

# 3. Enviar para GitHub
git push
```

---

## 🆘 **Problemas Comuns**

### **"Git não é reconhecido"**
- **Solução:** Instalar Git: https://git-scm.com/download

### **"Permission denied"**
- **Solução:** Usar Personal Access Token em vez da senha

### **"Repository not found"**
- **Solução:** Verificar se o nome do usuário e repositório estão corretos

### **"Nothing to commit"**
- **Solução:** Verificar se há arquivos para adicionar com `git status`

---

## 📱 **Resultado Final**

Depois de seguir estes passos:
- ✅ Código estará no GitHub
- ✅ Poderá fazer deploy na Vercel
- ✅ App funcionará no celular
- ✅ URL profissional para compartilhar

**Quer que eu ajude com algum passo específico?**
