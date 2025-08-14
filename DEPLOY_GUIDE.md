# 🚀 Como Fazer o Iluminavoz Funcionar no Seu Celular

## Opções de Deploy

### 1. 🌟 **Vercel (Recomendado - GRATUITO)**

A Vercel é a plataforma oficial do Next.js e oferece deploy gratuito com domínio personalizado.

#### Passos:

1. **Criar conta na Vercel:**
   - Acesse: https://vercel.com
   - Faça login com GitHub, GitLab ou Bitbucket

2. **Subir o código para o GitHub:**
   ```bash
   # No seu computador, dentro da pasta do projeto:
   git init
   git add .
   git commit -m "Initial commit - Iluminavoz app"
   
   # Criar repositório no GitHub e conectar:
   git remote add origin https://github.com/SEU_USUARIO/iluminavoz.git
   git push -u origin main
   ```

3. **Deploy na Vercel:**
   - Na Vercel, clique em "New Project"
   - Conecte seu repositório GitHub
   - A Vercel detectará automaticamente que é um projeto Next.js
   - Clique em "Deploy"
   - Em 2-3 minutos seu app estará online!

4. **Acessar no celular:**
   - A Vercel fornecerá uma URL como: `https://iluminavoz.vercel.app`
   - Acesse essa URL no seu celular
   - Funciona como um app nativo!

---

### 2. 🔥 **Netlify (Alternativa GRATUITA)**

#### Passos:
1. Acesse: https://netlify.com
2. Faça login e conecte seu GitHub
3. Selecione o repositório do Iluminavoz
4. Configure:
   - Build command: `npm run build`
   - Publish directory: `.next`
5. Deploy automático!

---

### 3. 📱 **PWA (Progressive Web App)**

Para uma experiência ainda mais nativa no celular, vou adicionar suporte PWA:

#### Vantagens:
- ✅ Instalar como app no celular
- ✅ Funciona offline (básico)
- ✅ Ícone na tela inicial
- ✅ Splash screen personalizada

---

### 4. 🏠 **Servidor Local (Para Testes)**

Se quiser testar localmente no celular:

1. **No seu computador:**
   ```bash
   npm run dev
   ```

2. **Descobrir seu IP local:**
   - Windows: `ipconfig`
   - Mac/Linux: `ifconfig`
   - Procure por algo como: `192.168.1.100`

3. **Acessar no celular:**
   - Conecte o celular na mesma rede WiFi
   - Acesse: `http://192.168.1.100:8000`

---

## 🎯 **Recomendação Final**

**Para uso real:** Use a **Vercel** - é gratuita, rápida e profissional.

**Para testes:** Use o servidor local.

## 📋 **Checklist de Deploy**

- [ ] Código no GitHub
- [ ] Deploy na Vercel
- [ ] Testar no celular
- [ ] Configurar domínio personalizado (opcional)
- [ ] Adicionar PWA (opcional)

## 🔧 **Próximos Passos Opcionais**

1. **Domínio personalizado:** `www.iluminavoz.com.br`
2. **Banco de dados real:** PostgreSQL, MongoDB
3. **Autenticação:** Login de pacientes
4. **Notificações:** Lembretes de consulta
5. **WhatsApp Integration:** Confirmação automática

---

**Quer que eu configure alguma dessas opções para você?**
