# TOUT #INSTALLER SUR MAC POUR #DEV

---

## Installer Xcode

    xcode-select --install

---

### installer OMZ

    sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

#### installer les fonts

    # clone
       git clone https://github.com/powerline/fonts.git --depth=1

    # install
       cd fonts
       ./install.sh

    # clean-up a bit
      cd ..
      rm -rf fonts

#### definir "agnoster" comme thème principal

    $ open ~/.zshrc
    - Puis remplacer ZSH_THEME="robbyrussell" par ZSH_THEME="agnoster"

---

### Installer Homebrew

    ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

---

### Installer rbenv

    brew install rbenv ruby-build

    echo 'if which rbenv > /dev/null; then eval "$(rbenv init -)"; fi' >> ~/.zshrc

    source ~/.zshrc

#### Installer Ruby

    rbenv install 3.0.2
    rbenv global 3.0.2
    ruby -v

#### Installer Rails

     gem install rails # install latest.
     rbenv rehash
     rails -v # Rails 6.1.4.1

---

### Configurer Git

    git config --global color.ui true
    git config --global user.name "username"
    git config --global user.email "YOUR@EMAIL.com"
    ssh-keygen -t rsa -C "YOUR@EMAIL.com"

#### Puis faire

    cat ~/.ssh/id_rsa.pub  # Et coller la clé dans ssh et gpg de github.

#### tester

     ssh -T git@github.com # Renvoie si ok : Hi excid3! You've successfully authenticated, but GitHub does not provide shell access.

---

### Installer NVM

     brew install nvm
     mkdir ~/.nvm # Répertoire de travail de NVM
     open ~/.zshrc

#### Ajouter

    # config nvm :
     export NVM_DIR="   HOME/.nvm"
     [ -s "/usr/local/opt/nvm/nvm.sh" ] && . "/usr/local/opt/nvm/nvm.sh"  # This loads nvm
     [ -s "/usr/local/opt/nvm/etc/bash_completion.d/nvm" ] && . "/usr/local/opt/nvm/etc/bash_completion.d/nvm"  # This loads nvm bash_completion

     source ~/.zshrc

### Installer Node

     nvm install lts/*
     nvm use lts/*
     node -v
     npm -v

#### Mettre à jour npm

     npm install -g npm@latest
     npm -v

---

## Installer les applications depuis brew

    brew install sqlite3
    brew install mysql
    brew install postgresql
    brew install --cask visual-studio-code
    brew install --cask google-chrome
    brew install --cask insomnia
    brew install --cask microsoft-edge
    brew install --cask zoom
    brew install --cask discord
    brew install --cask slack
    brew install --cask postico
    brew install --cask keka
    brew install --cask vlc
    brew install --cask qbittorrent
    brew install --cask webstorm
    brew install --cask rubymine
    brew install --cask mysqlworkbench
    brew install --cask adobe-creative-cloud

---

`Créé le 12 Octobre 2021 03:00PM par Maxime LESTAGE, France`
`À jour le 25 Novembre 2021 10:43PM par Maxime LESTAGE, France`
