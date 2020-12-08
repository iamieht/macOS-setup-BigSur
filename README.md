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
