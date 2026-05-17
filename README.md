VitexSoftware's repository source
=================================

![Logo](apt-repo-vitexsoftware.svg?raw=true)

This package sets up the VitexSoftware APT repository on Debian/Ubuntu systems.

## Installation

### Using the package (recommended)

```shell
sudo apt install lsb-release wget
sudo wget -O /usr/share/keyrings/vitexsoftware.gpg https://repo.vitexsoftware.com/KEY.gpg
sudo wget -O /etc/apt/sources.list.d/vitexsoftware.sources https://repo.vitexsoftware.com/vitexsoftware.sources
sudo apt update
sudo apt install apt-repo-vitexsoftware
```

### Manual setup (legacy `.list` format)

```shell
echo "deb [signed-by=/usr/share/keyrings/vitexsoftware.gpg] https://repo.vitexsoftware.com $(lsb_release -sc) main" | sudo tee /etc/apt/sources.list.d/vitexsoftware.list
sudo apt update
```

## Suites

| Suite    | Description                          |
|----------|--------------------------------------|
| stable   | Current Debian/Ubuntu codename       |
| borrow   | Cross-release packages               |

## Repository

`https://repo.vitexsoftware.com/`
