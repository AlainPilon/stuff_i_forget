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
and to get the styling for Operator Mono https://gist.github.com/brandondurham/3828ac42766f9f187c8e

Styling to use Operator Mono:

    atom-workspace,
    atom-text-editor {
        font-family: "OperatorMono-Light";
        font-weight: normal;
    }

    atom-panel.tool-panel {
    }

    .editor .comment,
    atom-text-editor.editor {
        font-family: "OperatorMono-Light";
        font-style: normal;
    }

    atom-text-editor.editor .syntax--comment {
        font-family: "OperatorMono-LightItalic";
        font-style: normal;
    }

    .syntax--keyword, .syntax--control, .syntax--attribute-name {
      font-style: italic;
    }
