### On the flow

*react app with ts template*

```
> npx create-react-app -template typescript project-name
> cd project-name
> yarn        # install dep
> yarn start  # start dev-server
> yarn build  # build app
```

*Into packages.json @types/* package*
Contain type definition of a lib


*Type definition lib/file* `*.d.ts`

```typescript
declare function saveData(data: string): void
```

*Add dependency*

```
> yarn add styled-components             # install packages
> yarn add @types/styled-components      # install def type, mandatory to skip TS error
```

### Define functional component

#### Functional component's type 
Type of functional component are infered by ts, as 

```typescript
export const Box = () => {
  return <div>Coucou<div>
}

export const Box: React.FC = () => {
  return <div>Coucou<div>
}

// React.FC = React.FunctionalComponent
```

#### Functional component noargs

```typescript
import React from 'react'
import ColumnContainer from 'styles'

export const Column = () => {
  return <ColumnContainer>Coucou<ColumnContainer>
}
```

#### Functional component with props

```typescript
import React from 'react'
import Box from 'styles'

interface BoxProps {
  text: String
}

export const Column = ({ text }: BoxProps ) => {
  return <Box>{text}<Box>
}
```

#### Functional component with children and props

```typescript
import React from 'react'
import Box from 'styles'

interface BoxProps {
  text: String
}

export const Column = ({text} : React.PropsWithChildren<BoxProps>) => {
  return ( 
    <Box><div>Coucou</div>{Children}<Box>
   )
}
```

#### Note: Type "inspection" 

```typescript
type React.PropsWithChildren<P> = P & {
  children?: React.ReactNode;
}
```

 * `?` optional == type P | undefined
 * `&` type intersection
 * `P` generic type serve as placeholder
 * `React.ReactNode` Node type, children are nodes ;)
 
The same as:

```typescript
interface BoxProps {
 text: String;
 children?: React.ReactNode
}
   





