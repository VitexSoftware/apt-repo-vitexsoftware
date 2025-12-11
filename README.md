VitexSoftware's repository source
=================================

![Logo](apt-repo-vitexsoftware.svg?raw=true)

This package sets up the VitexSoftware APT repository:

```shell
sudo apt install lsb-release wget

sudo wget -O /usr/share/keyrings/vitexsoftware.gpg http://repo.vitexsoftware.com/KEY.gpg
echo "deb [signed-by=/usr/share/keyrings/vitexsoftware.gpg] http://repo.vitexsoftware.com $(lsb_release -sc) main" | sudo tee /etc/apt/sources.list.d/vitexsoftware.list
sudo apt update
```
