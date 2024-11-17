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

## Solve plot problem with linux and NVIDIA optimus

OS: Debian 11 <br /> 
Distro: Mx Linux 21.2 <br />
Matlab version: R2020b <br />
Nvidia Model: GeForce RTX 3060 Mobile <br />
Intel chipset model: 12th Gen Intel(R) Core(TM) i9-12900H <br />

`export MESA_LOADER_DRIVER_OVERRIDE=i965; matlab`


## Fix install Matlab

OS: Debian 12 <br /> 
Distro: Mx Linux 23.3 <br />
Matlab version: R2024a <br />
Kernel version: 6.11.8-1-liquorix-amd64

we see this error in the installation:

```
terminate called after throwing an instance of 'std::runtime_error'
  what():  Failed to launch web window with error: Unable to launch the MATLABWindow application. The exit code was: 1
Aborted
```

to fix it:

```
cd <matlab-installation-dir>
cd sys/os/glnxa64
mkdir exclude
mv libstdc++.so.6 libstdc++.so.6.0.28 exclude


cd <matlab-installation-dir>
cd bin/glnxa64
mkdir exclude
mv libstdc++.so.6* exclude/
```
