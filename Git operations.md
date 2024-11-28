[Summarized from Video](https://www.bilibili.com/video/BV1r3411F7kn/?spm_id_from=333.999.0.0)
# Git operations
1.  Create a directory and direct Git Bash or terminal to this directory
```Bash
cd [Path]
```
2.  Configuration
set up the name and email
```bash
git config --global user.name [user-name]
git config --global user.email [user-email]
```
3. initialization
tell git to user version control of this directory
```
git init
```
- branch 'master' appears by default(main branch)
- hidden item '.git' is added to the directory

4. new documents 
echo "[content]" > [file_name]          version 1

check file status: branch, file status(untracked, committed)
```
git status
```

git add [file_name] 工作区-> 缓存区
git commit 添加提交信息， 进入vim, i -> represents insert, Esc 退出编辑, :wq-save and exit vim

git add [file_name]                    version 2
git add [file_name]                       version 3

git status  -> two kinds of status

git commit -m “[commit messages, record changes]”

git log      查看所有版本（author, versions, dates）

5. create .ignore document
```
touch .gitignore
```

add file names in .gitignore to ignore the document



6. add new branch

git branch [branch_name]           branch2
git branch: 查看所有分支
git checkout [branch_name] : enter new branch, all files in master branch will be copied 

delete the files in new branch
``` add and commit
git commit -a -m "[message]"
```
git checkout master:  all files will be back except the ignored file


git branch -d [branch_name]: delete the branch, with the merge alert

git branch -D [branch_name]: delete the branch directly, without confirmation

git checkout -b [branch_name]: create new branch and switch to this branch


add new content in this branch  (in the file )'version_temp', this won't appear in mmaster branch

git commit -a -m "[message]"     version_temp


check the content in master
git checkout master


merge [branch_name] to the current branch
git merge [branch_name]

add content in the file 'version master'
git commit -am "version master"
git checkout branch_temp   this content won't appear in branch_temp
git commit -am  “different content”

# GitHub operations
1. create repository
 equal to git init 

2. ‘download zip’ in GitHub will doanload the latest version of document, without log and records (without .git) 
git clone [https] : get all versions of files


add new content to this file  "version 2"
git commit -am "version 2"
3. git remote -v : check 
origin:   name of remote repository
set up tokens to push files 
Settings - Developer Settings - Personal access tokens - Generate new tokens - Select scopes - generate tokens
4. git push
5. git fetch: local file won't change

git diff origin/main   远程仓库名/分支名, get the difference from remote and local reposities

git pull  : get all content form remote repository




# VS code with Git and GitHub
1. open a folder
2. Source Control (left panel)-> initialize repository   => git init
3. U: Untracked, +: git add, -: cancel, A: staged , M: modified (in this status, click on the file name, different version of this file will be compared)
"message" -> commit
···  source control -> more actions-> branch -> create branch 
4. left down: change branch 
publish branch : git push 
