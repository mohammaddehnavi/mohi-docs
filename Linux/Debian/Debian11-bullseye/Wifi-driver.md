# Install Realtek wifi driver on Mx linux 23.1 (Debian 12)

I used [this repo](https://github.com/lwfinger/rtw89).

here is `uname -a` output:

`Linux mohi 6.1.0-13-amd64 #1 SMP PREEMPT_DYNAMIC Debian 6.1.55-1 (2023-09-29) x86_64 GNU/Linux`

```bash
sudo apt-get update
sudo apt-get install make gcc linux-headers-$(uname -r) build-essential git

git clone https://github.com/lwfinger/rtw89.git
cd rtw89
make
sudo make sign-install
```
