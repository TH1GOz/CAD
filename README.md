# Convite de 15 anos da Driellen — versão estática para Vercel

Esta versão não usa Vite, Rollup, npm, dependências nem etapa de compilação. A Vercel deve servir diretamente o `index.html` e a imagem `convite.png`.

## Arquivos na raiz do projeto

```text
Convite-namorada/
├── index.html
├── convite.png
├── vercel.json
└── README.md
```

## Corrigir as configurações da Vercel

No painel da Vercel, abra **Settings → Build and Deployment** e configure:

- **Root Directory:** `.` (raiz do repositório; não `rollup`, `public` ou outra pasta).
- **Framework Preset:** `Other`.
- Remova/limpe qualquer comando Build ou Install configurado manualmente no painel se ele não respeitar o `vercel.json`.

O `vercel.json` nesta versão escolhe o preset `Other`, desativa instalação/build e publica a raiz do projeto como saída. Assim não deve executar `npm install` nem `vite build`.

## Atualização do GitHub (importante)

Envie **os arquivos que estão diretamente nesta pasta** para a raiz do repositório que a Vercel usa. Não envie o diretório `convite_driellen_estatico` como uma pasta aninhada: `index.html`, `convite.png` e `vercel.json` precisam ficar no nível raiz selecionado pela Vercel.

Apague do repositório antigo os arquivos de build do projeto que não são necessários, principalmente:

- `package.json` e `package-lock.json` antigos, caso existam na raiz e sejam do projeto Vite/Rollup;
- `vite.config.js` ou `vite.config.ts` antigos, caso não sejam utilizados;
- pastas de dependências como `node_modules` se tiverem sido enviadas ao GitHub.

Não é necessário remover um pacote chamado Rollup de `node_modules` à mão; o objetivo é deixar de usar a cadeia de build antiga e garantir que a Vercel não esteja apontada para uma pasta `rollup`.

## Funcionalidades preservadas

- Convite original sem modificar a arte.
- Intro de carta antiga fechada por padrão; a animação e a revelação do convite só começam quando a pessoa clica no envelope ou no botão “Abrir convite”.
- Clique em “Click e confira o local” abre o Google Maps para: R. Célso Félix Moreno Farsoni, 12 - 09 - Q.ta Bela Olinda, Bauru - SP.
- Confirmação abre o WhatsApp `+55 14 99144-0905` com a mensagem `Eu confirmo a minha presença para o seu aniversário!!!`.
- Layout responsivo para celular e computador.

## Testar localmente

Ao abrir `index.html`, a carta permanece fechada até alguém clicar no envelope ou em “Abrir convite”. Para testar links e responsividade, abra o arquivo no navegador ou, com Node.js instalado, execute dentro desta pasta:

```bash
npx serve .
```

Como o projeto é estático, não execute `npm install` ou `npm run build`.
