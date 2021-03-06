### Stage to create a repository

Configure `.gitignore`

```
touch .gitignore
echo "/node_modules">> .gitignore
echo "yarn.lock" >> .gitignore
```

###### First commit

```
git add *
git commit -m "first commit"
git remote add origin git@github.com:zurgl/next-blog.git
git branch -M main
git push -u origin main
```
