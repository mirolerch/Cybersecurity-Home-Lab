# SOC Analyst Lab

Hands-on SOC analyst lab built for the PSAA certification.

## Course Outline

| # | Topic | Status |
|---|-------|--------|
| 01 | Lab Setup | ✅ Done |
| 02 | Security Operations Fundamentals | ⏳ Pending |
| 03 | Phishing Analysis | ⏳ Pending |
| 04 | Network Security | ⏳ Pending |
| 05 | Endpoint Security | ⏳ Pending |
| 06 | SIEM | ⏳ Pending |
| 07 | Threat Intelligence | ⏳ Pending |
| 08 | Digital Forensics | ⏳ Pending |
| 09 | Incident Response | ⏳ Pending |

## Lab Setup

### Installing Oracle VM VirtualBox

- [VirtualBox Downloads](https://www.virtualbox.org/wiki/Downloads)
- [Install VirtualBox on Mac](https://cs.hofstra.edu/docs/pages/guides/vbox_mac.html)
- [Install VirtualBox on Linux](https://phoenixnap.com/kb/install-virtualbox-on-ubuntu)
- [Visual C++ Redistributable](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170)

### Installing Windows

- [Windows 11 Enterprise Evaluation](https://www.microsoft.com/en-us/evalcenter/download-windows-11-enterprise)

### Configuring Windows

- [Git](https://git-scm.com/)
- [MalwareCube/SOC101](https://github.com/MalwareCube/SOC101)

```powershell
# Disable real-time protection
Set-MpPreference -DisableRealtimeMonitoring $true

# Disable scanning of network files
Set-MpPreference -DisableScanningNetworkFiles $true

# Disable block at first sight
Set-MpPreference -DisableBlockAtFirstSeen $true

# Disable Windows Defender AntiSpyware
reg add "HKLM\SOFTWARE\Policies\Microsoft\Windows Defender" /v DisableAntiSpyware /t REG_DWORD /d 1 /f

# Clone course repository
git clone https://github.com/MalwareCube/SOC101.git
```

> ZIP Password: `LCty2JmHQLB3uc9VxjeohENr`

### Installing Ubuntu

- [Ubuntu Desktop](https://ubuntu.com/download/desktop)
- [Past Ubuntu Releases](https://releases.ubuntu.com/)

```bash
sudo apt update
sudo apt install bzip2 tar gcc make perl git
sudo apt install linux-headers-generic
sudo apt install linux-headers-$(uname -r)
```

### Configuring Ubuntu

```bash
sudo apt install git
git clone https://github.com/MalwareCube/SOC101.git
chmod +x ./install.sh
./install.sh
```

> ZIP Password: `LCty2JmHQLB3uc9VxjeohENr`

### Configuring the Lab Network

Create a separate NAT Network in VirtualBox for isolated communication between the Windows and Ubuntu VMs.
