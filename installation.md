Установка ПО
===

1. [Homebrew](https://brew.sh/)
1. [git](https://git-scm.com)
1. [iTerm2](https://www.iterm2.com)
1. [Atom](https://atom.io)
1. [Node.js](https://nodejs.org/en/download/)

## Настройка

### SSH

[Создания](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/) ключа для авторизации.

Настройка агента для авторизации по ключам `~/.ssh/config`:
```
Host *
 AddKeysToAgent yes
 UseKeychain yes
 IdentityFile ~/.ssh/id_rsa
```

### Git

Настройка в `~/.gitconfig`:
```
[user]
  name = Dmitry Fitiskin
  email = dfitiskin@gmail.com
[core]
  excludefile = ~/.gitignore # Глобальный список файлов и папок, которые не нужны в репо
  autocrlf = input
[pull]
  rebase = true # делать rebase при git pull
```

Псевдонимы команд для `~/.gitconfig`:
```
[alias]
  s = status -s
  lg = log --oneline --decorate --graph
  lga = log --oneline --decorate --graph --all
  co = checkout
  diffs = diff --staged
  mergef = merge --no-ff
```

Глобальный список исключений для `~/.gitignore`:
```
node_modules
.settings/
.jshintrc
.project
.sublime-project
.tern-project
.DS-Store
.vscode/
```

### GitHub

[Добавление](https://help.github.com/articles/adding-a-new-ssh-key-to-your-github-account/) ключа в аккаунт.

### Atom

Настройка:
- Шрифт [FiraCode](https://github.com/tonsky/FiraCode) для лигатур

Плагины:
- emmet
- file-type-icons
- editorconfig
- quick-highlight

### iTerm2

Настройка:
- [powerlevel9k](https://gist.github.com/kevin-smets/8568070)
- убираем из powerlevel9k лишнее в `~/.zshrc`:
  ```
  POWERLEVEL9K_LEFT_PROMPT_ELEMENTS=(dir vcs)
  POWERLEVEL9K_SHORTEN_DIR_LENGTH=1
  POWERLEVEL9K_RIGHT_PROMPT_ELEMENTS=(status time)
  ```
- цветовой профиль [One Dark](./OneDark.itermcolors)

Плагины:
- [Auto suggestions](https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md#oh-my-zsh)

### Node.js

Настройка:
- npm в `~/.npmrc`:
  ```
  init.author.name=Dmitry Fitiskin
  init.author.email=dfitiskin@gmail.com
  init.license=MIT
  ```
