#Zellij config
## Requirements
- zellij
- fish

## Install Zellij
**Fedora**
```bash
sudo dnf copr enable varlad/zellij 
sudo dnf install zellij
```

## Clone the repo
```bash
git clone https://github.com/stkiegerl/zellij.git ~/.config/zellij
```

## Ingegration
Autostart a new zellij shell
bash
```bash
echo 'eval "$(zellij setup --generate-auto-start bash)"' >> ~/.bashrc
```

zsh
```zsh
echo 'eval "$(zellij setup --generate-auto-start zsh)"' >> ~/.zshrc
```
