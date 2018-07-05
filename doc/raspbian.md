Raspbian Config

# Set apt source mirror

Backup and edit source.list
```bash
sudo cp /etc/apt/source.list /etc/apt/source.list.backup
sudo nano /etc/apt/source.list
```
Comment original content and add two below lines at the end
```bash
deb http://mirrors.ustc.edu.cn/raspbian/raspbian/ stretch main contrib non-free rpi
deb-src http://mirrors.ustc.edu.cn/raspbian/raspbian/ stretch main contrib non-free rpi
```