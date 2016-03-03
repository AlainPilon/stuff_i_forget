# Git
## List the last commit of each branch, most recent first

    git for-each-ref --sort=committerdate refs/heads/ --format='%(HEAD) %(color:yellow)%(refname:short)%(color:reset) - %(color:red)%(objectname:short)%(color:reset) - %(contents:subject) - %(authorname) (%(color:green)%(committerdate:relative)%(color:reset))'

## Delete all local git branches

    git branch --merged master | grep -v master | xargs git branch -d
