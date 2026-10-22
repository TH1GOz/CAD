# Convite de 15 anos da Driellen

Site responsivo do convite de 15 anos, com uma introdução animada inspirada na abertura de uma carta antiga, arte original preservada, link do local no Google Maps e confirmação de presença pelo WhatsApp.

## Estrutura

```text
convite-driellen/
├── index.html
├── package.json
├── vercel.json
├── .gitignore
└── public/
    └── convite.png
```

## Testar no computador

Use Node.js 22. Dentro desta pasta, execute:

```bash
npm install
npm run dev
```

Para testar a versão de produção:

```bash
npm run build
npm run preview
```

O build gera a pasta `dist/`.

## Publicar na Vercel

Envie todos os arquivos desta pasta para a raiz do repositório GitHub. Na Vercel, confirme:

- **Root Directory:** a pasta que contém `package.json` (normalmente `.` / raiz do repositório).
- **Framework Preset:** Vite.
- **Install Command:** `npm install`.
- **Build Command:** `npm run build`.
- **Output Directory:** `dist`.

O `vercel.json` define o comando de instalação, build e pasta de saída. Se o painel da Vercel tiver configurações manuais diferentes, atualize-as ou remova as sobrescritas.

## Link do local

A área sobre “Click e confira o local” abre o Google Maps para:

`R. Célso Félix Moreno Farsoni, 12 - Q.ta Bela Olinda, Bauru - SP, 17023-750`

## Confirmação de presença

O botão do convite abre o WhatsApp para `+55 14 99144-0905` com a mensagem:

`Eu confirmo a minha presença para o seu aniversário!!!`
