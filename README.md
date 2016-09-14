# Git Practice

Practicing my `git` commands for branching and merging so I don’t break anything important.

## Creating the Repo

1. Repo was initialized with `git init`
2. Creating `README.md`
3. Added `README.md` to repo

        git add README.md

4. Repo created on [GitHub](https://github.com) through the web interface
5. Remote origin added with

        git remote add origin https://github.com/dustykeyboard/git-practice.git

6. Publish to GitHub repo

        git push -u origin master

## Creating a new *Feature Branch*

1. Start from `master` branch

        git checkout master && git pull

2. Create *feature branch*

        git checkout -b feature/readme-text

3. Make changes

        vi README.md

4. Commit changes

        git commit -a -m "Updated README text"

5. Push changes to feature branch on GitHub

        git push origin feature/readme-text

## Update from *Master Branch* and continue working

1. Continue working

        vi README.md

2. Get latest from `master`

        git checkout master && git pull
        git checkout feature/readme-text
        git stash
        git rebase -i master
        git stash pop

3. Commit changes to feature branch

        git commit -a -m "Adding latest from master"

4. Push changes to feature branch on GitHub

        git push origin feature/readme-text
