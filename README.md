# githubflow

# Reference doc
[A Branching and Releasing Strategy That Fits GitHub Flow](https://hackernoon.com/a-branching-and-releasing-strategy-that-fits-github-flow-be1b6c48eca2)

# Hands on
## feature 1
Different from a blog, open a branch for Feature 1 based on the main branch and develop it locally.

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

## feature 2
Following the instructions for blog article, development is done in the developer's own forked repository.
From the main repository, fork the main repository using another GitHub account, and create a branch named "feature/2" on the forked repository. Then, clone the forked repository from GitHub and proceed with development locally.

### clone fork repo by developer mattleeq
```bash
$ git clone git@github.com-mattleeq:mattleeq/githubflow.git githubflow.mattleeq
$ cd githubflow.mattleeq
```

### a2
```bash
$ git checkout -b feature/2
$ mkdir -p feature/2
$ echo "a2" > feature/2/a2.txt
$ git add feature/2/a2.txt README.md
$ git commit -m "feat: 2-a2"
```

### b2
```bash
$ echo "b2" > feature/2/b2.txt
$ git add feature/2/b2.txt README.md
$ git commit -m "feat: 2-b2"
```

### c2 & PR to main reop base on feature 2
```bash
$ echo "c2" > feature/2/c2.txt
$ git add feature/2/c2.txt README.md
$ git commit -m "feat: 2-c2"
$ git push origin feature/2
```
