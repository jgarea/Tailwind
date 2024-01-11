# Tailwind

## Primeros pasos

```powershell
npm init -y
npm install -D tailwindcss
```

`tailwind.css`

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

```powershell
npx tailwind init
```

`tailwind.config.js`

```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./*.html"],
  theme: {
    extend: {},
  },
  plugins: [],
};
```

```powershell
npx tailwindcss -i tailwind.css -o styles.css
npx tailwindcss -i tailwind.css -o styles.css --minify
```

## Con Vite

```powershell
npm -i -D vite postcss autoprefixer
npx tailwindcss init -p
```

package.json

```json
{
  "name": "tailwind",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "dev": "vite",
    "build": "vite build",
    "preview": "vite preview"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "devDependencies": {
    "autoprefixer": "^10.4.16",
    "postcss": "^8.4.33",
    "prettier": "^3.1.1",
    "prettier-plugin-tailwindcss": "^0.5.11",
    "tailwindcss": "^3.4.1",
    "vite": "^5.0.11"
  }
}
```

```powershell
npm run dev
```

`index.html`

```html
<link rel="stylesheet" href="tailwind.css" />
```

## Prettier

```powershell
npm install prettier -D
npx prettier --write index.html
```

prettier.config.js

```js
// prettier.config.js
module.exports = {
  plugins: ["prettier-plugin-tailwindcss"],
};
```

```powershell
npm install prettier-plugin-tailwindcss -D
```
