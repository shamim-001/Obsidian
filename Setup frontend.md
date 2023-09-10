#setup #tailwindcss 
[Reusable tailwind blocks](https://tailblocks.cc/)
[Tailwind tool box](https://www.tailwindtoolbox.com/)

```bash
npm create vite@latest .
```

or 
with typescript
```bash
npm create vite@latest my-project -- --template react-ts
```

cd my-project
```bash
npm install -D tailwindcss postcss autoprefixer prettier prettier-plugin-tailwindcss
```

```bash
npx tailwindcss init -p
```

// tailwind.config.js / extra
```bash
content: ["./index.html", "./src/**/*.{js,jsx,ts,tsx}"],
```

Remove all the css code form index.css and app.css

# index.css
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

[[jsmastery index.css]]
[[jsmastery style.js]]


```bash
// for development
npm run dev

// for building and deployment
npm run build
```

