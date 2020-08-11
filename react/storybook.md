Story Book
-----

### Purpose

Nice UI-component helper

### Basic setup

```bash
mkdir story-book
cd story-book/

yarn init -y
yarn add -D @storybook/react babel-core

yarn add react react-dom 

mkdir .storybook src
```

### Example folder tree

```bash
~/r/story-book ❯❯❯ tree -aI node_modules
.
├── package.json
├── src
│   ├── Button.js
│   └── Button.stories.js
├── .storybook
│   ├── config.js
│   └── WelcomeStory.js
└── yarn.lock
```


### File content

##### **package.json**
```
{    ...
  "scripts": {
    "storybook": "start-storybook -p 6006 -c .storybook"
  }
}
```



##### **src/Button.js**
```javascript
import React from 'react' 

export const Button = ({ bg, children }) => (
  <button style={{ backgroundColor: bg }}> {children}</button>
);
```


##### **src/Button.stories.js**
```javascript
import React from 'react'

import { storiesOf } from '@storybook/react'
import { Button } from './Button'


storiesOf('Button', module)
  .add('with background', () => (
  <Button bg="palegoldenrod">Hello World</Button>
))
  .add('with background-2', () => (
  <Button bg="blue">Hello World</Button>
))

```

##### **.storybook/config.js**
```javascript
import { configure } from '@storybook/react'

const req = require.context('../src', true, /.stories.js$/)

function loadStories() {
  require('./WelcomeStory');
  req.keys().forEach(file => req(file));
}

configure(loadStories, module);
```


##### **.storybook/Welcome.js**
```javascript
import React from 'react'
import { storiesOf } from '@storybook/react'


storiesOf('Main', module).add('Welcome', () => (
  <h3>Welcome into my story</h3>
))
```


### Run example

```bash
yarn storybook
```

### Addon not working to be tested

```bash
yarn add -D @storybook/addons storybook-addon-jsx
echo "import 'storybook-addon-jsx/register' " > .storybook/addons.js

```

to be continue ....

-------
## More Info 
[video](https://egghead.io/courses/design-systems-with-react-and-typescript-in-storybook)
