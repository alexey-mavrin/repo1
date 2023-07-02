# Useful Git commands

## Initial commands

Create new repository

```
mkdir repo && cd repo
git init
```

Link repo with a remote

```
git remote add origin git@github.com:alexey-mavrin/repo.git
```

where `origin` is the conventional name.
Note that `repo` should already exist.

## Branchs and commits

Set the default branch

```
git config init.defaultBranch main
```

Create commit

```
cat > file.txt << EOF
Hello
EOF

git add file.txt
git commit -m "file.txt: some change"
```

Push commits and link branch name and the remote

```
git push -u origin main
```

or just push commits

```
git push
```
