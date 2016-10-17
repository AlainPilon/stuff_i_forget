# Git
## List the last commit of each branch, most recent first

    git for-each-ref --sort=committerdate refs/heads/ --format='%(HEAD) %(color:yellow)%(refname:short)%(color:reset) - %(color:red)%(objectname:short)%(color:reset) - %(contents:subject) - %(authorname) (%(color:green)%(committerdate:relative)%(color:reset))'

## Delete all local git branches

    git branch --merged master | grep -v master | xargs git branch -d

# Atom

## Enable ligature with non ligatured fonts

    atom-text-editor::shadow .lines .keyword.operator {
        font-family: "FiraCode-Light";
        text-rendering: optimizeLegibility;
    }

    atom-text-editor::shadow .lines .cursor-line .keyword.operator {
        text-rendering: auto;
    }

(stolen from: http://netcell.github.io/2016/05/ligature-with-unsupported-font-in-atom/)
