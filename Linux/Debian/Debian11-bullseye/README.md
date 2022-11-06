# Debian 11 - bullseye

## Install openforti GUI

```bash
# Download latest version from here https://hadler.me/linux/openfortigui/
wget https://apt.iteas.at/iteas/pool/main/o/openfortigui/openfortigui_0.9.8-1_amd64_bullseye.deb

# Install
sudo dpkg -i openfortigui_0.9.8-1_amd64_bullseye.deb
```

## Fix issue for show snapd app in launcher

```bash
# Create link for X11 session
sudo ln -s /etc/profile.d/apps-bin-path.sh /etc/X11/Xsession.d/99snap

# Open this file 
sudo vim /etc/login.defs

# Add /snap/bin to ENV_PATH 
## Example:
ENV_PATH PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/snap/bin
```