#setup 

```
npx create-next-app@latest
```

![[nextjs_setup.png]]
All install
```bash
npm install eslint-config-standard eslint-plugin-tailwindcss eslint-config-prettier prettier
```

`.eslintrc.json`
```json
{
  "extends": [
    "next/core-web-vitals",
    "standard",
    "plugin:tailwindcss/recommended",
    "prettier"
  ],
  "rules": {
    "camelcase": [
      "error",
      {
        "allow": ["League_Spartan"]
      }
    ]
  }
}
```

[[Code Architecture]]

https://ui.shadcn.com/docs/installation/next
