# 🚀 OfertaMax — Deploy na Vercel

## Deploy em 3 passos

### Opção A — Deploy pelo site da Vercel (mais fácil, recomendado)

1. Acesse **vercel.com** e faça login/cadastro
2. Clique em **"Add New Project"**
3. Clique em **"Upload"** e faça upload desta pasta `frontend/`
4. A Vercel detecta automaticamente que é Next.js
5. Clique em **"Deploy"** — pronto! Site no ar em ~2 minutos

### Opção B — Deploy pelo terminal

```bash
# Instalar Vercel CLI
npm install -g vercel

# Entrar na pasta frontend
cd frontend

# Instalar dependências
npm install

# Fazer deploy
vercel --prod
```

---

## Estrutura do projeto

```
frontend/
├── pages/
│   ├── index.tsx     ← Página principal (Homepage + todas as rotas)
│   ├── _app.tsx      ← App wrapper
│   └── _document.tsx ← HTML base com fontes
├── styles/
│   └── globals.css   ← Todo o design system
├── public/           ← Arquivos estáticos
├── package.json      ← Dependências
├── next.config.js    ← Configuração Next.js
├── tsconfig.json     ← TypeScript config
└── vercel.json       ← Configuração Vercel
```

---

## Login de demonstração

| Tipo | Email | Senha |
|------|-------|-------|
| **Admin** | admin@ofertamax.com | qualquer senha |
| **Usuário** | qualquer email | qualquer senha (mín. 8 chars) |

---

## Variáveis de ambiente (opcionais)

No painel da Vercel, em **Settings → Environment Variables**, adicione:

| Variável | Valor | Para que serve |
|----------|-------|----------------|
| `NEXT_PUBLIC_API_URL` | URL do seu backend | Conectar com banco de dados real |
| `NEXT_PUBLIC_AFFILIATE_TAG` | seutag-20 | Código de afiliado Amazon |

---

## Como conectar ao backend (Railway)

1. Faça deploy do backend no Railway (railway.app)
2. Copie a URL do backend (ex: https://ofertamax-api.up.railway.app)
3. No painel Vercel → Settings → Environment Variables
4. Adicione: `NEXT_PUBLIC_API_URL` = URL do backend
5. Redeploy

---

## Custo estimado

| Serviço | Plano | Custo |
|---------|-------|-------|
| Vercel (frontend) | Hobby | **GRÁTIS** |
| Railway (backend) | Developer | ~R$ 25/mês |
| PostgreSQL | Railway | Incluso |
| Redis | Upstash Free | **GRÁTIS** |
| **Total mínimo** | | **GRÁTIS** |

---

## Funcionalidades incluídas no frontend

✅ Homepage com Hero, Oferta do Dia com timer, produtos reais da Amazon
✅ Página de produto com galeria de imagens, histórico de preço, comentários
✅ Página de categoria com filtros (desconto, avaliação, preço, Score IA)
✅ Sistema de login/cadastro
✅ Perfil com dropdown — Admin só aparece para admins
✅ Painel Admin completo (dashboard, produtos, usuários)
✅ Admin pode criar novos admins e promover usuários
✅ Favoritos, cupons com cópia, countdown timer
✅ Design dark profissional preto + laranja
✅ Mobile-first com navbar inferior
✅ Zero emojis nos ícones — SVG limpos
✅ Imagens reais da Amazon CDN
✅ Preços em R$ formato brasileiro
