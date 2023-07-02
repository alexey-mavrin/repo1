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

## HEAD

`HEAD` refers to two things in git.
1. File `.git/HEAD`, containing the reference to the file with the last commit made
2. The position in the current branch, from which successive commit will be made.

```
# cat .git/HEAD
ref: refs/heads/main

# cat .git/refs/heads/main
2ce5430bdd3a1344f84096361c244a411809cb0a
```
