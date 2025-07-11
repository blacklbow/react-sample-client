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

### tailwindcss

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
