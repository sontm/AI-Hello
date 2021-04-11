# AI-Hello
## MacM1 Environment Setup

Xcode build tools:
$ xcode-select --install

Install Brew:
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
$ brew update
brew upgrade git         || brew install git
brew upgrade gh          || brew install gh
brew upgrade wget        || brew install wget
brew upgrade imagemagick || brew install imagemagick
brew upgrade jq          || brew install jq
brew upgrade openssl     || brew install openssl
brew upgrade tree        || brew install tree
brew upgrade ncdu        || brew install ncdu
brew upgrade htop        || brew install htop
brew upgrade tig         || brew install tig
brew upgrade xz          || brew install xz
brew upgrade readline    || brew install readline

Install Zsh Terminal:
https://medium.com/@Clovis_app/configuration-of-a-beautiful-efficient-terminal-and-prompt-on-osx-in-7-minutes-827c29391961


Setup Git SSH:
$ mkdir -p ~/.ssh && ssh-keygen -t ed25519 -o -a 100 -f ~/.ssh/id_ed25519 -C "EMAIL"
$ pbcopy < ~/.ssh/id_ed25519.pub
$ Copy to Git Account

In order not to re-type your SSH passphrase
$ touch ~/.ssh/config
And then add these 3 lines to the file. Save.

Host *
  AddKeysToAgent yes
  UseKeychain yes


Install Ruby(optional):
$ brew uninstall --force rbenv ruby-build
$ brew install rbenv
$ rbenv install --list
$ rbenv install 2.7.2

Install NVM:
$ curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.37.0/install.sh | zsh
$ nvm install --lts

Install Python env:
Before installing Python, please check your xz version with:
$ brew info xz

It should be more than 5.2.0, if not you should run:

$ sudo rm -rf /usr/local/opt/xz
$ brew upgrade
$ brew install xz

Then run:

$ brew install readline

$ brew install pyenv
$ pyenv install 3.9.1
$ pyenv global 3.9.1

Pyvirtual env
$ git clone https://github.com/pyenv/pyenv-virtualenv.git $(pyenv root)/plugins/pyenv-virtualenv
$ pyenv virtualenv 3.9.1 AI
$ pyenv global AI

Py packages:
$ pip install --upgrade pip
Then let's install some packages for the first weeks of the program:
$ pip install pytest pylint ipdb pyyaml nbresult autopep8 flake8 lxml
Let's install packages useful for API & Scraping:
$ pip install requests bs4
Finally, more Data Science packages:
$ pip install jupyterlab pandas matplotlib seaborn plotly scikit-learn
That's it for today. During the bootcamp, we'll install more packages but we'll talk about that later.
If you want to check which packages (and which version of that package) you have installed, you can run:
$ pip freeze

----> If have Error Fix Error for M1
Install conda forge
https://github.com/conda-forge/miniforge

$ conda env list
$ conda create -n AI3.8 python=3.8.6
$ conda install -n AI3.8 scikit-learn pandas

$ pip install pytest pylint ipdb pyyaml nbresult autopep8 flake8 lxml
$ pip install requests bs4
$ pip install jupyterlab matplotlib seaborn plotly

$ conda activate AI3.8

Can follow https://claytonpilat.medium.com/tutorial-tensorflow-on-an-m1-mac-using-jupyter-notebooks-and-miniforge-dbb0ef67bf90

for Tensor Flow, install using https://github.com/apple/tensorflow_macos/tree/v0.1alpha2











