# u-centerをUbuntu22.04で使う
```
sudo wget -nc -O /etc/apt/keyrings/winehq-archive.key https://dl.winehq.org/wine-builds/winehq.key
sudo wget -nc -P /etc/apt/sources.list.d/ https://dl.winehq.org/wine-builds/ubuntu/dists/jammy/winehq-jammy.sources

sudo apt update
sudo apt install --install-recommends winehq-stable

sudo apt install winetricks

export WINEARCH=win32
export WINEPREFIX=$HOME/.wine-ucenter
winecfg
winetricks vcrun2019 openssl

wine /home/ubuntu/.wine/drive_c/Program\ Files\ \(x86\)/u-blox/u-center_v25.06/u-center.exe
```
