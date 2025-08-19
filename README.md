# sample-client

## 環境

```txt
node:23.11.0
pnpm:10.11.0
```

## 導入メモ

### vite

```sh
npm create vite@latest
```

#### index.htmlをsrc配下に移動

vite.confing.tsに追記

```ts
  root: './src',
```
参照を修正
index.html

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <link rel="icon" type="image/svg+xml" href="/vite.svg" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Vite + React + TS</title>
  </head>
  <body>
    <div id="root"></div>
    <script type="module" src="./main.tsx"></script>
  </body>
</html>
```

publicをsrc配下に移動

### tailwindcss

> https://nerdcave.com/tailwind-cheat-sheet

```sh
pnpm install tailwindcss @tailwindcss/vite
```

vite.config.tsの編集

```ts
import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react'
import tailwindcss from '@tailwindcss/vite'

// https://vite.dev/config/
export default defineConfig({
  plugins: [react(), tailwindcss()],
})
```

index.cssの編集(下記以外は削除する)

```css
@import "tailwindcss";
```

