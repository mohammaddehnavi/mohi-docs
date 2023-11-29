# Install Realtek wifi driver on Mx linux 23.1 (Debian 12)

I used [this repo](https://github.com/lwfinger/rtw89)

```bash
sudo apt-get update
sudo apt-get install make gcc linux-headers-$(uname -r) build-essential git

git clone https://github.com/lwfinger/rtw89.git
cd rtw89
make
sudo make sign-install
```
