##### Folder set up

At the projet root

```
mkdir .vscode
touch .vscode/settings.json
```

##### Basic settings

Into `settings.json` put

```
{
    "files.exclude": {
        ".vercel": true,
        ".next": true,
        "yarn.lock": true,
        "node_modules": true,
    }
}
```

