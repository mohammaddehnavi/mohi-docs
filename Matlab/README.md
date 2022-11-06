# Matlab

## Install psychtoolbox manually

OS: Debian 11 <br /> 
Distro: Mx Linux 21.2 <br />
Matlab version: R2020b <br />

```bash
# Download latest version of psychtoolbox
wget https://codeload.github.com/Psychtoolbox-3/Psychtoolbox-3/zip/refs/tags/3.0.18.13

# Unzip 
unzip Psychtoolbox-3-3.0.18.13.zip

# Move Toolbox to your matlab toolbox folder
sudo mv Psychtoolbox-3-3.0.18.13/Psychtoolbox/ /home/mohi/Matlab/R2020b/toolbox/

# Open your matlab with root account
sudo matlab

# Go to /home/mohi/Matlab/R2020b/toolbox/ with matlab and run:
SetupPsychtoolbox

# Checking installation
PsychtoolboxVersion
```