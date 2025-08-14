# 📱 Como Usar o Iluminavoz no Seu Celular

## 🚀 Opção 1: Deploy Rápido (Recomendado)

### Vercel (Gratuito e Profissional)

1. **Criar conta GitHub** (se não tiver):
   - Acesse: https://github.com
   - Clique em "Sign up"

2. **Subir o código:**
   ```bash
   # No terminal, dentro da pasta do projeto:
   git init
   git add .
   git commit -m "Iluminavoz - App de Fonoaudiologia"
   
   # Criar repositório no GitHub:
   # - Vá em github.com
   # - Clique no "+" > "New repository"
   # - Nome: "iluminavoz"
   # - Clique "Create repository"
   
   # Conectar e enviar:
   git remote add origin https://github.com/SEU_USUARIO/iluminavoz.git
   git branch -M main
   git push -u origin main
   ```

3. **Deploy na Vercel:**
   - Acesse: https://vercel.com
   - Clique "Continue with GitHub"
   - Clique "New Project"
   - Selecione "iluminavoz"
   - Clique "Deploy"
   - ⏰ Aguarde 2-3 minutos

4. **Pronto! 🎉**
   - Você receberá uma URL: `https://iluminavoz-xxx.vercel.app`
   - Acesse no seu celular
   - Funciona como app nativo!

---

## 📱 Opção 2: Teste Local

### Para testar rapidamente:

1. **No seu computador:**
   ```bash
   npm run dev
   ```

2. **Descobrir seu IP:**
   - Windows: Abra CMD e digite `ipconfig`
   - Mac: Abra Terminal e digite `ifconfig`
   - Procure algo como: `192.168.1.100`

3. **No celular:**
   - Conecte na mesma WiFi
   - Abra o navegador
   - Digite: `http://192.168.1.100:8000`

---

## 📲 Instalar como App (PWA)

Depois de acessar a URL:

### Android:
1. Abra no Chrome
2. Menu (3 pontos) > "Adicionar à tela inicial"
3. Confirme "Adicionar"

### iPhone:
1. Abra no Safari
2. Botão compartilhar (quadrado com seta)
3. "Adicionar à Tela de Início"
4. Confirme "Adicionar"

---

## ✨ Funcionalidades no Celular

- ✅ **Agendamento de consultas**
- ✅ **Exercícios de fonoaudiologia**
- ✅ **Design responsivo**
- ✅ **Funciona offline (básico)**
- ✅ **Ícone na tela inicial**
- ✅ **Splash screen**

---

## 🔧 Próximos Passos (Opcionais)

1. **Domínio personalizado:** `www.iluminavoz.com.br`
2. **Banco de dados:** Para salvar agendamentos reais
3. **Notificações push:** Lembretes de consulta
4. **WhatsApp:** Integração para confirmações

---

## 🆘 Precisa de Ajuda?

**Problemas comuns:**

- **"Não carrega no celular":** Verifique se está na mesma WiFi
- **"Erro 404":** Confirme se o servidor está rodando
- **"Não instala como app":** Use Chrome (Android) ou Safari (iPhone)

**Quer que eu configure algo específico?** Me avise! 😊
