##### Add the required lib

```
yarn add -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
mkdir styles
touch styles/tailwind.css
touch styles/css_custom_data.json
code .
```



```
git push
git commit -m "add tailwind"
git add *
```


```
  purge: [
    './pages/**/*.{js,jsx,ts,tsx}',
    './components/**/*.{js,jsx,ts,tsx}',
  ],
```

`settings.json`
```
{
    "files.exclude": {
        ".vercel": true,
        ".next": true,
        "yarn.lock": true,
        "node_modules": true,
    },
    "css.customData": [".vscode/css_custom_data.json"]
}
```

`css_custom_data.json`
```
{
    "version": 1.1,
    "atDirectives": [
      {
        "name": "@tailwind",
        "description": "Use the `@tailwind` directive to insert Tailwind's `base`, `components`, `utilities` and `screens` styles into your CSS.",
        "references": [
          {
            "name": "Tailwind Documentation",
            "url": "https://tailwindcss.com/docs/functions-and-directives#tailwind"
          }
        ]
      },
      {
        "name": "@responsive",
        "description": "You can generate responsive variants of your own classes by wrapping their definitions in the `@responsive` directive:\n```css\n@responsive {\n  .alert {\n    background-color: #E53E3E;\n  }\n}\n```\n",
        "references": [
          {
            "name": "Tailwind Documentation",
            "url": "https://tailwindcss.com/docs/functions-and-directives#responsive"
          }
        ]
      },
      {
        "name": "@screen",
        "description": "The `@screen` directive allows you to create media queries that reference your breakpoints by **name** instead of duplicating their values in your own CSS:\n```css\n@screen sm {\n  /* ... */\n}\n```\n…gets transformed into this:\n```css\n@media (min-width: 640px) {\n  /* ... */\n}\n```\n",
        "references": [
          {
            "name": "Tailwind Documentation",
            "url": "https://tailwindcss.com/docs/functions-and-directives#screen"
          }
        ]
      },
      {
        "name": "@variants",
        "description": "Generate `hover`, `focus`, `active` and other **variants** of your own utilities by wrapping their definitions in the `@variants` directive:\n```css\n@variants hover, focus {\n   .btn-brand {\n    background-color: #3182CE;\n  }\n}\n```\n",
        "references": [
          {
            "name": "Tailwind Documentation",
            "url": "https://tailwindcss.com/docs/functions-and-directives#variants"
          }
        ]
      },
      {
        "name": "@layer",
        "description": "Allow to define custom utilies for a selected layer\n",
        "references": [
          {
            "name": "Tailwind Documentation",
            "url": "https://tailwindcss.com/docs/functions-and-directives#layer"
          }
        ]
      }
  
    ]
  }
```


