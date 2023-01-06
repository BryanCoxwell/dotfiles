# dotfiles

The dotfiles here are managed through a [bare git repo](https://www.atlassian.com/git/tutorials/dotfiles) to avoid having to worry about symlinking or anything else.

The `git` command to add/commit/push files is aliased to `config`:
```
"alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME'"
```
