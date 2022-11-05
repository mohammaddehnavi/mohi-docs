# Quartus

## Installation

OS: Debian 11 <br /> 
Distro: Mx Linux 21.2 <br />
Modelsim version: QuartusSetup-18.0.0.614-linux.run <br />

```bash
# Install dependencies
sudo apt install libc6:i386 libncurses6:i386 libxtst6:i386 libxft2:i386 libstdc++6:i386 libc6-dev-i386 lib32z1 libncurses5 libbz2-1.0:i386 libpng16-16 libqt5xml5 liblzma-dev libcanberra-gtk-module

# Give execute permission
chmod +x QuartusSetup-18.0.0.614-linux.run

# Install
./QuartusSetup-18.0.0.614-linux.run
```

- Note: After installation is complete, run the Quartus shortcut on your desktop, If Quartus doesn't start follow these steps:

```bash
# Go to Quartus directory
cd /home/mohi/intelFPGA/18.0/quartus/bin

# Run Quartus manually
./quartus
```

If you see this error `quartus: error while loading shared libraries: libpng12.so.0: cannot open shared object file: No such file or directory` you need to install libpng12 manually 

```bash
# Download libpng12 manually
## download link: http://mirrors.kernel.org/ubuntu/pool/main/libp/libpng/libpng12-0_1.2.54-1ubuntu1_amd64.deb
## then exract and copy libpng12.so.0, libpng12.so.0.54.0 from data.tar.gz folder(data/lib/x86_64-linux-gnu) to /usr/lib/x86_64-linux-gnu/

# Or use files in ./Assets in my repo :), then copy to /usr/lib/x86_64-linux-gnu/
cp ./Assets/* /usr/lib/x86_64-linux-gnu/
```

- Note: If you need your NIC card ID for your license to these steps: 

```bash
# Run ip command to show your NIC interface
ip a

# Then copy your mac address wihtout ":"
# Example NIC ID : 58:11:22:de:7c:b4
# Example NIC ID for the license file: 581122de7cb4
```

Then you can run Quratus correctly :)

