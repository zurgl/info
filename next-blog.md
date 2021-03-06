## Start from scratch

###### Install lib

```bash
mkdir blog
cd blog
yarn add next react react-dom
```
###### Add script to `package.json`

```json
{
  "scripts": {
    "dev": "next dev",
    "build": "next build",
    "start": "next start"
  }
}
```

###### Add an home page

```
mkdir home
touch home/index.js
```

content of `index.js`

```js
export default function Home() {
  return <h1>Hello World</h1>
}
```
###### Start the live server

```
yarn dev -- -p 3333
```


