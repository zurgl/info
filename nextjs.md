### nextjs projet creation

### from template

```bash
yarn create nextjs-app vanilla
```


### from scratch
```bash
yarn init
yarn add next react react-dom
```



### Configure vscode
mkdir .vscode
```json
// setting.json
{
    "files.exclude": {
        "node_modules/": true,
        "yarn.lock": true,
        ".next": true,
        "yarn-error.log": true,
    },
    "css.customData": [".vscode/css_custom_data.json"]
}
```

yo

```json
// css_custom_data.json.json
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


### Adding tailwind
##### Install file
```bash
yarn add tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

##### Configure purge

```js
// tailwind.config.js
    purge: [
      './pages/**/*.{js,jsx,ts,tsx}',
      './components/**/*.{js,jsx,ts,tsx}',
    ],
```

##### Import into nextjs


### For dev
yarn dev

### For production
yarn build
yarn start
