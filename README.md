# Ubuntu Setup
This repo has information on how to setup ubuntu the way I like.

## Run Initial Script (TODO)
### Install Zsh.
```
sudo apt install zs
chsh -s $(which zsh)
```
Now log out and back in.

### Install Oh-My_Zsh.
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### Install Powerline Fonts.
```
sudo apt-get install fonts-powerline
```

### Install Powerline10k Theme
```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/powerlevel10k
echo 'source ~/powerlevel10k/powerlevel10k.zsh-theme' >>~/.zshrc
```

### Get more packages available.
```
sudo add-apt-repository ppa:aslatter/ppa
```

### Fix tmux
```
cd
git clone https://github.com/gpakosz/.tmux.git
ln -s -f .tmux/.tmux.conf
cp .tmux/.tmux.conf.local .
```

### Install github CLI.
```
curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo dd of=/usr/share/keyrings/githubcli-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null
sudo apt update
sudo apt install gh
```




