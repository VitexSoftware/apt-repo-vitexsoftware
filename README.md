VitexSoftware's repository source
=================================

![Logo](apt-repo-vitexsoftware.svg?raw=true)

This package sets up the VitexSoftware APT repository on Debian/Ubuntu systems.
During installation a dialog lets you choose which repository components to enable.
Run `dpkg-reconfigure apt-repo-vitexsoftware` at any time to change your selection.

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

## Configuration

After installation, `/etc/apt/sources.list.d/vitexsoftware.sources` is generated
from your selections. To change them:

```shell
sudo dpkg-reconfigure apt-repo-vitexsoftware
```

### Components

| Component  | Description                                      |
|------------|--------------------------------------------------|
| main       | Core VitexSoftware packages                      |
| backports  | Packages backported from newer Debian releases   |
| games      | Game packages                                    |

### Suites

| Suite    | Description                                          |
|----------|------------------------------------------------------|
| *distro* | Current Debian/Ubuntu codename (e.g. `trixie`)       |
| borrow   | Cross-release packages not tied to a specific suite  |

## Repository

`https://repo.vitexsoftware.com/`
