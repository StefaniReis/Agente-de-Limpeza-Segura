# 🛡️ Limpeza Segura — Telegram Mini App

App de segurança do trabalho para diaristas.
Funciona como Mini App dentro do Telegram, com IA gratuita (Google Gemini).

---

## 📁 Estrutura de arquivos

```
limpeza-segura/
├── api/
│   ├── chat.js      ← Backend que chama o Gemini (IA)
│   ├── webhook.js   ← Bot do Telegram
│   └── setup.js     ← Configura o webhook (roda 1 vez)
├── public/
│   └── index.html   ← O app completo com toda a interface
├── package.json
├── vercel.json
└── README.md
```

---

## ✅ O que você vai precisar (o cliente já deve ter)

- Token do bot Telegram (ex: `7845123456:AAHdqTcvCH1vGWJxfSeofSBqMDuoJ5B7AB8`)
- Chave da API Gemini (ex: `AIzaSyB7xKpQmN3vL8wR2cE9hJ4tF6uY1iO5pA`)
- Conta no Vercel (conta já criada pelo cliente)

---

## 🚀 Passo a passo para o desenvolvedor

### 1. Subir o código no GitHub

```bash
git init
git add .
git commit -m "Limpeza Segura v1.0"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/limpeza-segura.git
git push -u origin main
```

### 2. Fazer deploy no Vercel

1. Acesse vercel.com e entre na conta do cliente
2. Clique em **"New Project"**
3. Clique em **"Import Git Repository"** e selecione o repositório criado acima
4. Clique em **Deploy** (sem mudar nada)
5. Aguarde o deploy. Você vai receber uma URL tipo: `https://limpeza-segura.vercel.app`

### 3. Configurar as variáveis de ambiente no Vercel

No painel do Vercel, vá em:
**Settings → Environment Variables** e adicione:

| Nome da variável    | Valor                          |
|---------------------|--------------------------------|
| `TELEGRAM_BOT_TOKEN`| Token recebido do BotFather    |
| `GEMINI_API_KEY`    | Chave da API do Google Gemini  |
| `APP_URL`           | URL do Vercel (ex: https://limpeza-segura.vercel.app) |

Após adicionar, clique em **Redeploy** para aplicar.

### 4. Configurar o webhook do Telegram (roda 1 vez só)

Após o redeploy, acesse no navegador:

```
https://limpeza-segura.vercel.app/api/setup
```

Você deve ver uma resposta JSON assim:
```json
{
  "mensagem": "Setup concluído com sucesso!",
  "webhook": { "ok": true, "result": true }
}
```

### 5. Testar

1. Abra o Telegram e pesquise pelo username do bot (ex: @LimpezaSeguraOficialBot)
2. Mande `/start`
3. O bot vai responder com um botão **"🛡️ Abrir Limpeza Segura"**
4. Ao tocar no botão, o app abre dentro do Telegram com toda a interface

---

## 🔑 Variáveis de ambiente necessárias

```env
TELEGRAM_BOT_TOKEN=7845123456:AAHdqTcvCH1vGWJxfSeofSBqMDuoJ5B7AB8
GEMINI_API_KEY=AIzaSyB7xKpQmN3vL8wR2cE9hJ4tF6uY1iO5pA
APP_URL=https://limpeza-segura.vercel.app
```

---

## 💰 Custos

| Item                | Custo       |
|---------------------|-------------|
| Vercel (hospedagem) | Grátis      |
| Telegram Bot API    | Grátis      |
| Gemini 1.5 Flash    | Grátis até 1.500 mensagens/dia |
| Domínio próprio     | ~R$ 40/ano (opcional) |

**Total mensal: R$ 0,00** ✨

---

## ⚙️ Funcionalidades do app

- 💬 **Chat com IA** — responde sobre qualquer produto de limpeza
- 📷 **Identificação por foto** — tira foto dos produtos e a IA identifica
- 🏠 **Memória por casa** — lembra os produtos de cada cliente
- 🚨 **SOS** — botão de emergência com primeiros socorros e telefones
- 🗄️ **Base de conhecimento** — adicione suas próprias normas
- 📅 **Agenda** — cadastro de clientes com horários e valores

---

## 📱 Como as diaristas usam

1. Baixar o Telegram (grátis)
2. Clicar no link: `t.me/SEU_BOT_USERNAME`
3. Tocar em **Iniciar**
4. Tocar em **"🛡️ Abrir Limpeza Segura"**
5. Pronto! O app abre com toda a interface

---

## 🆘 Suporte

Em caso de dúvidas sobre o código, entre em contato com quem desenvolveu o projeto.
