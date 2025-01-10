Cầu hình máy:
- CPU 2 core
- Ram 4GB
- Linux ubuntu 22.04

1. Update

```
sudo apt-get update && sudo apt-get upgrade -y
```
2. Install GUI

```
sudo apt install lightdm
```
```
sudo systemctl start lightdm
```
```
sudo apt-get install ubuntu-desktop
```

4. Cài đặt Remote Desktop
```
sudo apt-get install xrdp
```

5. Mở Remote Desktop trên PC và login bằng user là "root" và mật khẩu vps của bạn

6. Mở terminal trong Ubuntu desktop và Cài đặt apt repository (coppy từng dòng)
   
```
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
```

```
echo \ "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \ $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \ sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
```

```
sudo apt-get update
```

7. Cài đặt docker

```
sudo apt-get install docker.io -y
```

8. Mở trình duyệt firefox và tải open ledger Node về giải nén ra.
   
9. Coppy file .deb ra ngoài
    
10. Cài đặt Node

```
cd Downloads/
sudo dpkg -i openledger-node-1.0.0.deb
```
11. star Node

```
cd
openledger-node --no-sandbox
```

12. Đăng nhập vào setup như trong video là xong


