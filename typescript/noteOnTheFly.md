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





