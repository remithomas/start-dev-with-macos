# Start development with macOS

> ~~Sometimes~~ _One time_ you need links and how to install it !!

## Basic Tools

- [Homebrew](https://brew.sh) to install a lot of stuff !!!

```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

- [GIT](https://git-scm.com/download/mac)
- nodejs or using via [nvm](https://github.com/creationix/nvm): Node Version Manager
- [docker](https://docs.docker.com/docker-for-mac/install/)

## GIT

- [autocompletion](https://github.com/bobthecow/git-flow-completion/wiki/Install-Bash-git-completion) 

    - `brew install git && brew install bash-completion`
    - copy this in `~/.bash_profile`

```bash
if [ -f ~/.git-completion.bash ]; then
  . ~/.git-completion.bash
fi
```

- Colored branches in `~/.bash_profile`

```bash
parse_git_branch() {
    git branch 2> /dev/null | sed -e '/^[^*]/d' -e 's/* \(.*\)/ (\1)/'
}
export PS1="\u@\h \W\[\033[32m\]\$(parse_git_branch)\[\033[00m\] $ "
```

## Tools to create PR

- [ImageOptim](https://imageoptim.com/) to optimize **EVERY** images
- [LICEcap](https://www.cockos.com/licecap/) to record your screen before send a Pull request. 

## GraphQL

- [GraphiQl](https://electronjs.org/apps/graphiql)
```bash
brew cask install graphiql
````

## Note

> You could wipe to linux also ;)

## ToDO

- [ ] A bash script to install my stuff (why not)
