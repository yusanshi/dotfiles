# dotfiles

Refer: <https://www.atlassian.com/git/tutorials/dotfiles>

```bash
cd ~
git clone --bare git@github.com:yusanshi/dotfiles.git .dotfiles
echo 'alias gitdf="/usr/bin/git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME"' >> .bashrc
source .bashrc
gitdf config --local status.showUntrackedFiles no

# restore files
gitdf checkout main -- .gitignore .gitconfig ...

# view a file
gitdf show main:.bashrc
gitdf show main:.bashrc | cat

# add part of changes in a file
gitdf add -p .bashrc # y: add, n: not add, q: quit, not add current and following
```
