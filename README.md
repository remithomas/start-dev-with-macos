# Start development with macOS

> ~~Sometimes~~ _One time_ you need links and how to install it !!

- [Basic Tools](#basic-tools)
- [MacOS](#macos)
    - [Hidden files](#hidden-files)
    - [Quicklook (macOS)](#quicklook-macos)
- [GIT](#git)
- [Tools to create PR](#tools-to-create-pr)
- [GraphQL](#graphql)
- [Vscode](#vscode)
    - [Config](#config)
    - [Launch config](#launch-config)
    - [Plugins](#plugins)
- [Note](#note)
- [ToDO](#todo)

## Basic Tools

- [Homebrew](https://brew.sh) to install a lot of stuff !!!

```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

- [GIT](https://git-scm.com/download/mac)
- nodejs or using via [nvm](https://github.com/creationix/nvm): Node Version Manager
- [docker](https://docs.docker.com/docker-for-mac/install/)
- [npm autocompletion](https://docs.npmjs.com/cli/completion) `npm completion >> ~/.bashrc`

## MacOS

### Hidden files

- Open a terminal and type: `defaults write com.apple.finder AppleShowAllFiles YES`
- then relaunch your finder (using ctrl + click on finder icon)

From this [website](https://ianlunn.co.uk/articles/quickly-showhide-hidden-files-mac-os-x-mavericks/)

### Quicklook (macOS)

- [Markdown](http://inkmarkapp.com/markdown-quick-look-plugin-mac-os-x/)
- [JSON](http://www.sagtau.com/quicklookjson.html)
- [CSV](https://code.google.com/archive/p/quicklook-csv/)
- [Plain text](https://whomwah.github.io/qlstephen/) if has no extension

[Complete list](http://www.quicklookplugins.com) or [Awesome list](https://github.com/sindresorhus/quick-look-plugins)

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
- [trailer app](https://github.com/ptsochantaris/trailer) show Pull requests from Github.

## GraphQL

[GraphiQl](https://electronjs.org/apps/graphiql) download link.
```bash
brew cask install graphiql
```

## Vscode

### Config

Some config in preference

```json
{
    "editor.renderWhitespace": "all",
    "files.insertFinalNewline": true,
    "eslint.autoFixOnSave": true,
    "files.trimFinalNewlines": true,
    "tslint.enable": true,
    "tslint.autoFixOnSave": true,
    "markdown-preview-enhanced.liveUpdate": true
}
```

### Launch config

Useful when want debug, launch: [launch.json](vscode/launch.json)

### Plugins

- Auto Close Tag `formulahendry.auto-close-tag`
- Auto Rename Tag `formulahendry.auto-rename-tag`
- Color Info `bierner.color-info`
- CSS Peek `pranaygp.vscode-css-peek`
- Debugger for Chrome `msjsdiag.debugger-for-chrome`
- Docker `PeterJausovec.vscode-docker`
- Editorconfig for Vscode `EditorConfig.editorconfig`
- ESLint `dbaeumer.vscode-eslint`
- IntelliSense for CSS class names in HTML `Zignd.html-css-class-completion`
- Path Intellisense `christian-kohler.path-intellisense`
- Sort lines `Tyriar.sort-lines`
- Stylelint `shinnn.stylelint`
- vscode-icons `robertohuertasm.vscode-icons`

## Note

> You could wipe to linux also ;)

## ToDO

- [ ] A bash script to install my stuff (why not)
