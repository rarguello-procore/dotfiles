# Dotfiles

My dotfiles.

## Install Windows 11
Download Windows 11 Disk Image (ISO) for x64 devices from https://www.microsoft.com/en-us/software-download/windows11

Install Windows 11 (24H2) from `Win11_24H2_English_x64.iso`:

```
b56b911bf18a2ceaeb3904d87e7c770bdf92d3099599d61ac2497b91bf190b11  Win11_24H2_English_x64.iso
```

Create a USB to install Windows 11 using WoeUSB: https://github.com/WoeUSB/WoeUSB

```bash
sudo ./woeusb-5.2.4.bash --device Win11_24H2_English_x64.iso /dev/sda --target-filesystem ntfs
```

## Configure
Install Windows Subsystem for Linux (WSL):

```powershell
wsl --install
```

Enable Winget configuration:

```powershell
winget --configure enable
```

## Winget configuration

```powershell
winget configure -f .\.configurations\configuration.dsc.yaml
```
