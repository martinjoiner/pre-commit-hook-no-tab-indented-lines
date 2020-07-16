# A pre-commit hook that stops you committing new tab-indented lines

**The rationale:** If you move code snippets via chat, Stackoverflow, markdown files, Gists or PRs or if your team work on a mix of Windows, Mac and Linux machines or if your team use a mix of various code editors and IDEs then indenting with spaces is the only way to guarantee the code aligns consistently wherever it goes. 

**The trap:** If you are actively maintaining or porting from a legacy codebase with a mix of tab and space-indented lines it is far too easy to accidentally author tab-indented lines. IDEs have some great settings to help but they will never be a strict gate-keeper. 

**My solution:** A pre-commit hook that simply does not pass tab-indented code. It only checks *new* lines of code and if it finds a tab-indented one, it aborts the commit and reports which lines need to be corrected. 

![Screen shot of terminal demonstrating pre-commit hook](/docs/Terminal-Screen-Shot.png "Terminal showing pre-commit hook catching tab-indented code")

## Installation

Simply copy the __pre-commit__ file into your repository's githooks folder (usually `.git/hooks/`) and give it execute permissions. Now it will be invoked on every commit. 

```
# From the root folder of your repo...
cd .git/hooks
```

If you have wget installed...
```
wget https://raw.githubusercontent.com/martinjoiner/pre-commit-hook-no-tab-indented-lines/main/pre-commit .
```

If no wget, try cURL instead...
```
curl https://raw.githubusercontent.com/martinjoiner/pre-commit-hook-no-tab-indented-lines/main/pre-commit -o pre-commit
```

Give the file execute permissions
```
chmod +x pre-commit
cd ../../
```

To learn more about githooks visit https://git-scm.com/docs/githooks 
