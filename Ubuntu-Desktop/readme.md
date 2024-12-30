1. Update

```
sudo apt-get update && sudo apt-get upgrade -y
```

2. Cài Docker
```
sudo apt-get install docker.io -y
```
3. Add user
```
adduser petertran
```
```
sudo usermod -aG sudo petertran
```
4. Install GUI

```
sudo apt install lightdm
```
```
sudo systemctl start lightdm
```
```
sudo apt-get install ubuntu-desktop
```


5. Cài đặt Remote Desktop
```
sudo apt-get install xrdp
```
6. Mod cổng 53579 và bỏ cổng 22 mặc định
Note: Nếu vẫn muốn sài cổng 22 thì không cần chạy cái này chỉ cần chạy lênh phía trên xong thì reboot lại.

```
sudo sed -i 's/3389/53579/g' /etc/xrdp/xrdp.ini
```
```
sudo sed -i 's/#Port 22/Port 53572/g' /etc/ssh/sshd_config
```
```
sudo ufw allow 53572 && sudo ufw allow 53579 && sudo ufw enable && sudo ufw status numbered
```
```
sudo reboot
```
7. Đăng nhập bằng remote desktop
Cú pháp: <địa chỉ IP>:53579 (nếu không đổi cổng tì chỉ cần địa chỉ IP)


