# CONFIG TAILWIND

**Site do Tailwind:** [Tailwind CSS - Documentation](https://tailwindcss.com/docs)

## Instalação no Terminal

Criar o pacote de projeto usando o comando:
`npm init`

Após isso instale o Tailwind CSS no seu projeto:

```terminal
npm install -D tailwindcss
npx tailwindcss init
```

## Módulo

```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

ou

```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

- **O asterisco simples:** é um caractere curinga que representa qualquer sequência de caracteres em um padrão de correspondência de arquivos. Ele é usado para fazer a correspondência de arquivos com base em um padrão específico.
- **O duplo asterisco:** quando usado em padrões de correspondência de arquivos, representa a correspondência recursiva em diretórios e subdiretórios. Isso significa que todos os diretórios e subdiretórios serão pesquisados para encontrar arquivos que correspondam ao padrão especificado.

## Adicionar Componentes no CSS

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

## Processo de Build

Toda vez que for trabalhar no seu site, será necessário rodar o comando o tailwindcss para processar e renderizar as estilizações no CSS:
`npx tailwindcss -i ./src/input.css -o ./src/output.css --watch`

Poderá também configurar o Package para que configure o comando de Build no **Scripts** como nesse exemplo:
`"tailwindcssRun": "npx tailwindcss -i ./css/style.css -o ./css/output.css --watch"`.

Com isso basta rodar o `npm run tailwindcssRun`
