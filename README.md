## Git - 1

**Version Control and Collaboration**
Chages vs Snapshots

- changes: Storing data as changes to the base version
- snapshots: Storing data as snapshots(git)

collaboration

- local : working in local computer
- centralized: using central VCS server
- distributed: interact with server computer and computers(git)

**Tree Staes in Git**

![https://git-scm.com/book/en/v2/images/areas.png](https://git-scm.com/book/en/v2/images/areas.png)

check pre-installed version

```bash
$ git --version
```

**Git confing**

Three levels

1. System level: — system option. Affects all uses and repositories on the system (administrative)
2. Global(user) level: — global option. Affects all repositories of a current user
3. Loval level: — local option. Specific to the current repository

Each level overrides values in the previous level: system -> global -> local

**Initalizing a repository in an existing directory**

```bash
$ git init
```

**checking repository status**

```bash
$ git status
```

**adding a new file to be staged**

```bash
$ git add[file_name]
$ git add . #all file
```

**unstaging a file**

```bash
$ git rm --cached[file_name]
```

**ignoring a file**

```bash
$ [file] .gitignore #파일디렉토리 안에다가
```

**commit**

```bash
$ git commit -m "commit message"
$ git log #cheaking commit contents
```

**branch**

```bash
$ git branch #cheaking
$ git branch -m master main #change branch name(master to main)
```

## Git - 2

### Removing files frome repository

- Use “git rm” instead of “rm” for removing a file from both file system and repository.
- This actually removes files from your disk.
- Use “git rm --cached” to keep files in the file system, but untrack them
- Use “git mv” to rename files
    
    ```bash
    $ git mv words.text new_words.text
    ```
    
- Use “git log” to check all commit history (with SHA-1 checksum)

### Unstaging a staged file

- git reset HEAD <file>
- git add.
- git restore --staged <file>

**Unmodifying a modified file (Discarding changes)**

- git restore <file>
    - this command discards changes you made.

**Git Push to Remote Repository**

```bash
$ git remote add origin https://github.com/leten02/git-practice.git

$ git push -u origin main
```
