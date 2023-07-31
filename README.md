# jaron's new mac setup

This repo contains all the scripts I use to set up a new Mac, and to keep my dotfiles in sync across my computers. I use [chezmoi](https://www.chezmoi.io/) to manage the dotfiles, bitwarden for secrets, and [Homebrew](https://brew.sh/) to install apps.

## Set up new Mac

1. Sign in to iCloud and App Store
2. Install all macOS updates.
3. Launch App Store and sign in, otherwise installing apps via [mas](https://github.com/mas-cli/mas) won’t work.
4. Install Bitwarden and sign in.
5. Quit Terminal (if it's running), and give it full disk access in System Preferences -> Security & Privacy -> Privacy tab -> Full Disk Access
6. Download [Ruby on Mac](https://www.rubyonmac.dev) Ultimate into the `Download` directory and run it with:

```shell
cd ~/Downloads/rubyonmac-ultimate
/bin/bash install
```

7. Now install `chezmoi`:

```shell
brew install chezmoi
```

and initialize it with:

```shell
chezmoi init https://github.com/jaronschulz/mac-setup.git
```

1. Run `rubyonmac` script again, but this time:

```shell
cd ~/Downloads/rubyonmac-ultimate /bin/bash install-newmac
```

9. Restart the computer.

In the future run `rom script` to update Ruby on Mac and all packages.
