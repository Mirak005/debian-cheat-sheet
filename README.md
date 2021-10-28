# debian-cheat-sheet

## Debian Setup for developers

## 1-Update source list

source : https://www.itzgeek.com/how-tos/linux/debian/setup-debian-11-official-repository-in-sources-list-etc-apt-sources-list.html

## 2- Install wifi

```sh
$ apt update && apt install firmware-iwlwifi
$ modprobe -r iwlwifi ; modprobe iwlwifi
```

source : https://wiki.debian.org/iwlwifi

## Google Chrome

```sh
$ wget -qO - https://dl.google.com/linux/linux_signing_key.pub | sudo gpg --dearmor -o /usr/share/keyrings/googlechrome-linux-keyring.gpg

$ echo "deb [arch=amd64 signed-by=/usr/share/keyrings/googlechrome-linux-keyring.gpg] http://dl.google.com/linux/chrome/deb/ stable main" | sudo tee /etc/apt/sources.list.d/google-chrome.list

$ sudo apt update

$ sudo apt install -y google-chrome-stable
```

source : https://www.itzgeek.com/how-tos/linux/debian/how-to-install-google-chrome-on-debian-11.html

## GIT

```sh
$ sudo apt install git-all
```

## 5-VS CODE

source : https://linuxize.com/post/how-to-install-visual-studio-code-on-debian-10/

## 6-Node js

```sh
$ curl -fsSL https://deb.nodesource.com/setup_16.x | sudo -E bash -
$ sudo apt-get install -y nodejs
```

source : https://github.com/nodesource/distributions/blob/master/README.md

## 7-NVM

```sh
$ curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash
$ source ~/.bashrc
```

source : https://github.com/nodesource/distributions/blob/master/README.md

## Sound issues (speaker)

```sh
$ sudo nano /etc/default/grub
## set GRUB_CMDLINE_LINUX_DEFAULT="quiet splash snd_hda_intel.dmic_detect=0"
```

source :https://askubuntu.com/questions/1243369/sound-card-not-detected-ubuntu-20-04-sof-audio-pci

## 5-Share screen issues

```sh
$ sudo nano /etc/gdm3/daemon.conf
##  uncomment WaylandEnable=false
```

source : https://linuxconfig.org/how-to-disable-wayland-and-enable-xorg-display-server-on-ubuntu-18-04-bionic-beaver-linux

NB :

- please make sure to run after the installation apt update
- Some installation needs a reboot of your system
