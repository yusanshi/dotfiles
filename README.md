# dotfiles

Refer: <https://www.atlassian.com/git/tutorials/dotfiles>

```bash
cd ~
git clone --bare https://github.com/yusanshi/dotfiles .dotfiles
echo 'alias gitdf="/usr/bin/git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME"' >> .bashrc
source .bashrc
gitdf config --local status.showUntrackedFiles no

# restore files
gitdf checkout main -- .gitignore .gitconfig ...

# view a file
gitdf show main:.bashrc
gitdf show main:.bashrc | cat

# add part of changes in a file
git add -p .bashrc # y: add, n: not add, q: quit, not add current and following
```
