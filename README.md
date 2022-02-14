![Logo](apt-repo-vitexsoftware.svg?raw=true)

VitexSoftware's repository source
=================================

This package do only this:


```shell
sudo apt install lsb-release wget

sudo wget -O /usr/share/keyrings/vitexsoftware.gpg http://repo.vitexsoftware.cz/keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/vitexsoftware.gpg]  http://repo.vitexsoftware.com  $(lsb_release -sc) main" | sudo tee /etc/apt/sources.list.d/vitexsoftware.list
sudo apt update
```


