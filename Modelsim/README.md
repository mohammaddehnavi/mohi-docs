# Modelsim 

## Installation

OS: Debian 11 <br /> 
Distro: Mx Linux 21.2 <br />
Modelsim version: ModelSimSetup-20.1.1.720-linux.run <br />

```bash

# Install dependencies
sudo dpkg --add-architecture i386
sudo apt-get update
sudo apt-get install libc6:i386 libncurses5:i386 libstdc++6:i386 lib32ncurses6 libxft2 libxft2:i386 libxext6 libxext6:i386 

# Give execute permission
chmod +x ModelSimSetup-20.1.1.720-linux.run

# Export PATH or copy the below line to your .bashrc
export PATH=$PATH:/home/mohi/intelFPGA/20.1/modelsim_ase/linux
```