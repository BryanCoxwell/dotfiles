# dotfiles

The dotfiles here are managed through a [bare git repo](https://www.atlassian.com/git/tutorials/dotfiles) to avoid having to worry about symlinking or anything else.

The `git` command to add/commit/push files is aliased to `config`:
```
"alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME'"
```

To install on a new system:
1. Commit the above alias to `.bashrc` or `.zsh`
2. Make sure git ignores the directory the repo will be cloned to: `echo ".cfg" >> .gitignore`
3. Clone: `git clone --bare https://github.com/BryanCoxwell/dotfiles/t $HOME/.cfg`
4. Checkout: `config checkout`
5. Set `showUntrackedFiles` to no on the local repo: `config config --local status.showUntrackedFiles no`
