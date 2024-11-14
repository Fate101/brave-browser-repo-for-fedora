# Brave Browser Repo for Fedora
> [!WARNING]  
> This is ***Not*** endorsed by Brave Software and is not official.
> You have been warned.

## Summary
So the way that [Brave tells you to install the Brave Browser](https://brave.com/linux/#fedora-rockyrhel) doesn't work anymore (I believe since Fedora 40 but idk). So I did the required edits to the repo file and written down the commands to add it.
Why? I get bored and reinstall my Operating Systems every so often. So here ya go!

## Changes
Just removed the `autorefresh=1` line. You can do it yourself and then just do `--from-repofile=.\brave-browser.repo` if you want to do it yourself.

**BRAVE PLEASE FIX THIS**

## Installation

### Release
```
sudo dnf install dnf-plugins-core

sudo dnf config-manager addrepo --from-repofile=https://raw.githubusercontent.com/Fate101/brave-browser-repo-for-fedora/refs/heads/main/brave-browser.repo

sudo rpm --import https://brave-browser-rpm-release.s3.brave.com/brave-core.asc

sudo dnf install brave-browser
```

### Beta
```
sudo dnf install dnf-plugins-core

sudo dnf config-manager addrepo --from-repofile=https://raw.githubusercontent.com/Fate101/brave-browser-repo-for-fedora/refs/heads/main/brave-browser-beta.repo

sudo rpm --import https://brave-browser-rpm-beta.s3.brave.com/brave-core-nightly.asc

sudo dnf install brave-browser-beta
```

### Nightly
```
sudo dnf install dnf-plugins-core

sudo dnf config-manager addrepo --from-repofile=https://raw.githubusercontent.com/Fate101/brave-browser-repo-for-fedora/refs/heads/main/brave-browser-nightly.repo

sudo rpm --import https://brave-browser-rpm-nightly.s3.brave.com/brave-core-nightly.asc

sudo dnf install brave-browser-nightly
```
