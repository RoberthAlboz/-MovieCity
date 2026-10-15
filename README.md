# MovieCity — Landing Page de Filmes

Landing page responsiva para um serviço de streaming fictício, criada como exercício de **React**, **componentização** e **CSS puro**. A proposta visual apresenta a marca MovieCity, navegação, chamada principal e uma grade de pôsteres de filmes.

> **Observação sobre este pacote:** o ZIP recebido contém a imagem de referência (`Landing_Page.png`), o roteiro do projeto (`roteiro_filmes.pdf`) e os arquivos de imagem. Ele **não contém o código-fonte React nem `package.json`**; portanto, não é possível iniciar a aplicação diretamente a partir deste pacote. As instruções abaixo descrevem como executar o projeto completo depois de obter ou criar esses arquivos.

## Visão geral

A página foi planejada com duas áreas principais:

- **Cabeçalho:** logotipo MovieCity, links para Filmes, Categoria, Sobre e Contato, botão Login e menu hambúrguer em telas menores.
- **Conteúdo principal:** texto de apresentação (“Seus Filmes”), botão “Mais” e grade com seis pôsteres.

Em telas menores, o conteúdo se adapta: as colunas se empilham, os pôsteres passam a ocupar duas colunas e a navegação é apresentada por um menu hambúrguer.

## Tecnologias previstas

- React 19
- Vite 7
- JavaScript com módulos ES (ESM)
- CSS puro, incluindo media queries
- ESLint

Não são previstas bibliotecas de interface como Bootstrap ou Tailwind; o projeto propõe praticar a estilização diretamente com CSS.

## Conteúdo incluído neste pacote

```text
landing_page_filmes/
├── imagens/
│   ├── afterlife.jpg
│   ├── harrypotter.jpg
│   ├── mowgli.jpg
│   ├── shift.png
│   ├── squidgame.webp
│   └── transformers.jpg
├── Landing_Page.png       # imagem de referência do layout
├── roteiro_filmes.pdf     # roteiro de implementação
└── README.md
```

Para a aplicação completa, o roteiro prevê uma estrutura semelhante a esta:

```text
src/
├── assets/                 # pôsteres usados pelo CSS
├── components/
│   ├── Header.jsx
│   ├── Main.jsx
│   └── Home.jsx
├── App.jsx
├── index.css
└── main.jsx
index.html
package.json
vite.config.js
eslint.config.js
```

## Pré-requisitos

Para executar a aplicação completa, instale:

- **Node.js 20.19+ ou 22.12+** (requisito do Vite 7)
- npm, incluído na instalação do Node.js

Confira as versões no terminal:

```bash
node -v
npm -v
```

## Como executar o projeto completo

Depois de obter ou criar o código-fonte React — incluindo o `package.json` — abra um terminal na pasta que contém esse arquivo e execute:

```bash
npm install
npm run dev
```

O Vite exibirá no terminal o endereço local, normalmente [`http://localhost:5173`](http://localhost:5173). Mantenha o terminal em execução enquanto trabalha; as alterações são atualizadas no navegador pelo HMR.

> Como o código-fonte e o `package.json` não estão neste ZIP, os comandos não funcionarão diretamente dentro da pasta extraída deste pacote.

## Scripts esperados

Quando disponíveis no `package.json` do projeto completo:

| Comando | Descrição |
|---|---|
| `npm run dev` | Inicia o servidor local de desenvolvimento com HMR. |
| `npm run lint` | Executa as verificações do ESLint. |
| `npm run build` | Gera a versão de produção na pasta `dist/`. |
| `npm run preview` | Pré-visualiza localmente o build de produção. |

## Imagens dos pôsteres

O roteiro prevê que os pôsteres sejam colocados em `src/assets/` e referenciados pelo CSS com caminhos relativos, por exemplo `url(./assets/afterlife.jpg)`. No pacote recebido, os arquivos estão em `imagens/`; para seguir a estrutura do roteiro, copie-os para `src/assets/` no projeto completo.

Arquivos fornecidos:

- `afterlife.jpg`
- `transformers.jpg`
- `mowgli.jpg`
- `shift.png`
- `squidgame.webp`
- `harrypotter.jpg`

A imagem `Landing_Page.png` serve como referência visual e `roteiro_filmes.pdf` contém o passo a passo detalhado de implementação.

## Responsividade e acessibilidade

O layout prevê ajustes em diferentes larguras, com breakpoints descritos no roteiro em 1100 px, 900 px, 600 px e 380 px. A implementação deve conferir o comportamento em desktop, tablet e celular, evitando rolagem horizontal.

O menu móvel é controlado por estado do React; o botão deve informar seu nome acessível e o estado de expansão (`aria-label` e `aria-expanded`) e fechar a navegação após a seleção de um link.

## Testes recomendados

No projeto completo:

```bash
npm run lint
npm run build
```

Depois, teste a interface no navegador em larguras como 1440 px, 1024 px, 768 px, 600 px e 375 px. No celular, verifique o menu hambúrguer e a grade de pôsteres.

## Ideias para evoluir

- Exibir título, descrição e classificação nos cards.
- Carregar filmes de uma API e renderizar os cards dinamicamente.
- Transformar os cards em um carrossel horizontal no celular.
- Usar elementos interativos acessíveis nos cards e considerar `prefers-reduced-motion` para animações.

## Licença

Nenhuma licença foi informada nos arquivos recebidos. Defina uma licença antes de redistribuir o projeto ou seus materiais, especialmente as imagens dos pôsteres.
