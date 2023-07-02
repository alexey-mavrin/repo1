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

# Git info and glossary

## Commit Hash

Commit Hash is the long hex string, uniquely identified the commit.
It corresponds to SHA-1 checksum.

## Git log

To get the commit history, use the following command:
```
git log
```

This command presents the list of commit, starting from the most recent;
for each commit, it shows
- commit hash
- commit author
- date of the commit
- commit message

Note: it is worth mentioning, that one can use shortened version of git hash,
long enough for uniquely select the commit in this particular repo. Those shortened
hashes could be produced by `git log --oneline` command.
