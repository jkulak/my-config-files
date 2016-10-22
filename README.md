# My configuration snippets

{{TOC}}

Remember to `$ source ~/.bash_profile` after adding new lines!

## GIT

### Add custom aliases (for displaying logs)

In your ~/.gitconfig file:

```bash
[alias]
    ll = log --pretty=oneline --abbrev-commit
    lg = log --pretty=oneline --abbrev-commit --graph --decorate --date=relative
    lgt = log --graph --pretty=format:'%Cred%h%Creset %s %Cgreen(%cr)%Creset' --abbrev-commit --date=relative
    lgtt = log --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr)%Creset' --abbrev-commit --date=relative
    lgf = log --graph --all --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(bold white)— %an%C(reset)%C(bold yellow)%d%C(reset)' --abbrev-commit --date=relative
```

### Enable autocompletion

In your ~/.bash_profile

```bash
# You need to download download the file from: https://github.com/git/git/blob/master/contrib/completion/git-completion.bash
source ~/.git-completion.bash
```

## BASH

### Customise your prompt

In your ~/.bash_profile:

```bash
# Prompt customization
# You need to download download the file from: https://github.com/git/git/blob/master/contrib/completion/git-prompt.sh
 
source ~/.git-prompt.sh
PS1='\u, \W $(__git_ps1 "\e[30;42m(%s)\e[m ")\e[0;35m$\e[m '
```