# macOS Setup (Big Sur)

A collection of configuration steps (so I don't forget them) for my macOS development environment.

## System Preferences

In **Apple Icon > System Preferences:**

- **Mouse** -> Uncheck Scroll direction: Natural
- **Security & Privacy** -> FileVault: Turn On
- **Security & Privacy** -> Firewall: Turn On

In **Finder > Preferences**:

- General:
  - Show these items on the desktop: *Hard disks*
  - Change *New finder window show* to open in your *Home Directory*
- Sidebar -> Add *Home*
- Advanced -> *Show all filename extensions*

## Xcode

For installing Xcode command line tools run:

```bash
xcode-select --install
```

## Homebrew

### Installation

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Once installation is complete, run the following command to make sure everything works:

```bash
brew doctor
```

## Git

```bash
brew install git
```

Initial configuration:

```bash
git config --global user.name "Your Name Here"
git config --global user.email "your_email@youremail.com"
```

## Applications

**Code Editor**

- Visual Studio Code:

```bash
brew install --cask visual-studio-code
```

**Terminal**

- iTerm2:

```bash
brew install --cask iterm2
```

Configuration:

In **iTerm2 > Preferences > Profiles:**

- Copy Default Profile
- Window: Columns 125 / Rows: 35

**Oh My Zsh**

- Install zsh

```bash
brew install zsh
````

- Install Oh My Zsh

```bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
````

- Install Powerline fonts

```bash
git clone https://github.com/powerline/fonts.git --depth=1
cd fonts
./install.sh
cd ..
rm -rf fonts
```

- Install Meslo Nerd Font patched for Powerlevel10k

Download these four ttf files:

- [MesloLGS NF Regular.ttf](https://github.com/romkatv/dotfiles-public/raw/master/.local/share/fonts/NerdFonts/MesloLGS%20NF%20Regular.ttf)
- [MesloLGS NF Bold.ttf](https://github.com/romkatv/dotfiles-public/raw/master/.local/share/fonts/NerdFonts/MesloLGS%20NF%20Bold.ttf)
- [MesloLGS NF Italic.ttf](https://github.com/romkatv/dotfiles-public/raw/master/.local/share/fonts/NerdFonts/MesloLGS%20NF%20Italic.ttf)
- [MesloLGS NF Bold Italic.ttf](https://github.com/romkatv/dotfiles-public/raw/master/.local/share/fonts/NerdFonts/MesloLGS%20NF%20Bold%20Italic.ttf)

Double-click on each file and press "Install". This will make MesloLGS NF font available to all applications on your system. Configure your terminal to use this font:

- **iTerm2**: Type p10k configure, answer Yes when asked whether to install Meslo Nerd Font and restart iTerm2 for the changes to take effect. Alternatively, open iTerm2 → Preferences → Profiles → Text and set Font to MesloLGS NF.
- **Visual Studio Code**: Open File → Preferences → Settings, enter terminal.integrated.fontFamily in the search box and set the value to MesloLGS NF.

- Install Powerlevel10k theme

Installation

```bash
brew install romkatv/powerlevel10k/powerlevel10k
echo 'source /usr/local/opt/powerlevel10k/powerlevel10k.zsh-theme' >>~/.zshrc
If your .zshrc sets ZSH_THEME, remove that line.
Restart Zsh
Type p10k configure if the configuration wizard doesn't start automatically.
````

**vlc**

```bash
brew install --cask vlc
````
**Jdownloader**
```bash
brew install --cask jdownloader
```
**Browsers**
```bash
brew install --cask google-chrome firefox
````




