# 🛠️ Dotfiles Git Manager

A elegant way to manage your dotfiles using only Git - no extra tools or symlinks needed!

## ✨ Features

- 🔄 Zero dependencies (just Git)
- 🔗 No symbolic links required
- 🌳 Support for different branches per machine
- 💾 Automatic backup and synchronization
- 📝 Complete change history
- 🚀 Easy installation across systems

## 🎯 Quick Setup

```bash
git init --bare $HOME/.cfg
alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME/.cfg'
config config --local status.showUntrackedFiles no
echo "alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME/.cfg'" >> $HOME/.bashrc
```

## 📚 Daily Usage

After setup, manage your dotfiles like this:

```bash
config add .vimrc
config commit -m "Update vimrc configuration"
config push
```

## 🚀 Migration to New System

1. Add the alias to your shell:
```bash
alias config='/usr/bin/git --git-dir=$HOME/.cfg/ --work-tree=$HOME/.cfg'
```

2. Clone your repository:
```bash
git clone --bare <your-repository-url> $HOME/.cfg
```

3. Checkout your dotfiles:
```bash
config checkout
```

> 💡 **Note**: If there are conflicts, existing files will be automatically backed up.

## ⚡ Pro Tip: Automated Installation

### How to do it

1. **Prepare & Host the script**
- Save the above script as `install.sh`
- You can host it on a GitHub Gist
- Use a URL shortening service like bit.ly
- Or host it on your own server

2. **Quick installation**
```bash
curl -Lks http://your-script-instalation | /bin/bash
```

### What the Installation Script Does:

- 🔍 Performs system compatibility checks
- 💾 Creates automatic backups of existing files
- 🐚 Supports multiple shells (bash, zsh, etc.)
- 🔒 Includes security verifications
- 📊 Provides detailed installation feedback

## 🤝 Contributing

Feel free to open issues or submit pull requests if you have suggestions for improvements!

## 📝 License

This project is under the MIT License - see the [LICENSE](LICENSE) file for details.
