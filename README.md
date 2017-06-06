# Pre-commit hook for teams working on a mix of Windows and Mac machines

A pre-commit hook that does not pass tab-indented code. 

Avoiding tab-indentation is the best way to ensure code looks the same on all code editors/viewers including Mac, Windows, Vim and the GitHub website. 

![Screen shot of terminal demonstrating pre-commit hook](/docs/Terminal-Screen-Shot.png "Terminal showing pre-commit hook catching tab-indented code")

## How to use

Simply copy the __pre-commit__ file in this repo into your repository's githooks folder (usually `.git/hooks/`) and give it execute permissions. Now it will be invoked on every commit. 

```
# From the root folder of your repo...
cd .git/hooks
wget https://raw.githubusercontent.com/martinjoiner/portable-code-pre-commit-hook/master/pre-commit .
chmod +x pre-commit
cd ../../
```

To learn more about githooks visit https://git-scm.com/docs/githooks 
