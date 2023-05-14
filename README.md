# githubflow

# 原始文章
[A Branching and Releasing Strategy That Fits GitHub Flow](https://hackernoon.com/a-branching-and-releasing-strategy-that-fits-github-flow-be1b6c48eca2)

# 文章實測操作
## feature 1
直接在 main repo 上開一個 branch，命名為 feature/1，並在 local 上開發  
註: 
blog 的說明，是在 develop fork 的 repo 上開發。這邊直接在 main repo 上開 feature 與開發  
>>
Pull Requests
We adopted Pull Requests, having each developer work in their own fork of the repo. This allows developers to create whatever branches they want without polluting the main fork of the repository.
### a1
```bash
$ git checkout -b feature/1
$ mkdir -p feature/1
$ echo "a1" > feature/1/a1.txt
$ # update README.md
$ git add feature/1/a1.txt README.md
$ git commit -m "feat: 1-a1"
```
### b1 & PR for feature 1
```bash
$ echo "b1" > feature/1/b1.txt
$ # update README.md
$ git add feature/1/b1.txt README.md
$ git commit -m "feat: 1-b1"
$ git push origin feature/1
```
