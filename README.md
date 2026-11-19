# PyHTools

![Image](.images/PyHTools.png)

- Python Hacking Tools (PyHTools) (pht) is a collection of python written hacking tools consisting of network scanner, arp spoofer and detector, dns spoofer, code injector, packet sniffer, network jammer, email sender, downloader, wireless password harvester credential harvester, keylogger, download&execute, and reverse_backdoor along with website login bruteforce, scraper, web spider etc. PHT also includes malwares which are undetectable by the antiviruses.

![PHT Image](.images/Windows_CLI-main.png)

- The tools provided are for educational purposes only. The developers are no way responsible for misuse of information and tools provided. All the information and tools are meant to help users to learn concepts. Use tools wisely!

- These tools are written in python3, refer installation to install/download tools and its dependencies.

- PyHTools comes with UI, but you can also use command line to use tools individually.

**`NOTE` : The UI hasn't been updated yet with new tools, and evil files so using cli is preferred.**

## How To Videos

- Gain access to remote shell over the Internet using HTTP Backdoor

  [![YT Thumbnail](https://img.youtube.com/vi/Wg-PiywAqyw/maxresdefault.jpg)](https://youtu.be/Wg-PiywAqyw)

---

## 💻 System Requirements / Requisitos de Sistema

### 🇺🇸 English — Minimum & Recommended Configuration

The architecture of **PyHTools** supports three hardware profiles depending on whether you run individual Python CLI modules, perform active network/Android instrumentation labs, or compile standalone packages with **PyInstaller / Nuitka**:

| Resource | 🟢 Minimum (Individual CLI Modules — Web/Network Basics) | 🟡 Intermediate (Network MITM / Sniffer / Android Frida Lab) | 🔵 Recommended (Full Suite + PyInstaller / Nuitka Builds) |
| :--- | :--- | :--- | :--- |
| **CPU** | **1 to 2 vCPUs** (`x86_64` / `arm64`) | **2 to 4 vCPUs** (`x86_64` / `arm64`) | **4+ vCPUs** (`x86_64`) |
| **RAM** | **1 GB to 2 GB RAM** | **4 GB RAM** | **8 GB+ RAM** |
| **Storage (SSD)** | **500 MB free** (Python 3 + core pip dependencies) | **2 GB free** (dependencies + wordlists + capture logs) | **5 GB+ SSD** (C compiler toolchain for Nuitka + PyInstaller + lab files) |
| **GPU (Optional)** | Not required | Not required | Not required |
| **Operating System** | Linux (Kali/Ubuntu/Debian), Windows 10/11, or Termux (limited) | Kali Linux or Ubuntu 22.04/24.04 LTS (`root` / `sudo` recommended) | Kali Linux (Rolling) or Ubuntu 24.04 LTS (isolated lab VM) |

#### 📦 Resource Usage by Architecture Component
- **Core CLI & Network Attackers/Detectors (`scapy`, `kamene`, ARP/DNS spoofer, packet sniffer, scanner)**: ~40 MB to 150 MB RAM; requires `root` / Administrator privileges and raw socket / promiscuous NIC access.
- **Web Scanners & Crawlers (`requests`, `beautifulsoup4`, login bruteforcer, spider, crawler)**: ~50 MB to 200 MB RAM depending on wordlist size and concurrency.
- **Android MITM & Instrumentation (`frida-tools`, `pure-python-adb`)**: ~80 MB to 250 MB RAM (plus connected ADB device/emulator).
- **Executable Packaging (`pyinstaller` / `nuitka`)**: ~400 MB to 1.5 GB RAM during compilation (`nuitka` also requires a native C compiler such as `gcc` or MSVC).

#### 🛠️ Software Dependencies
- **Core Runtime**: `Python 3.6+` (recommended `3.9+`), `pip`, `git`
- **Python Packages (`requirements.txt`)**: `scapy >= 2.4.5`, `kamene >= 0.32`, `requests >= 2.25.1`, `beautifulsoup4 >= 4.9.3`, `colorama`, `prettytable`, `pyfiglet`, `psutil`, `pynput`, `frida-tools`, `pure-python-adb`, `pytelegrambotapi`, `zstandard`, `pyinstaller`, `nuitka`
- **OS-Specific Optional Dependencies**: `netfilterqueue` + `libnetfilter-queue-dev` + `iptables` (Linux-only MITM/jammer/injector), `wmi` + `Npcap` (Windows), `gcc` / `build-essential` (for Nuitka builds)

### 🇧🇷 Português (BR) — Configuração Mínima & Recomendada

A arquitetura do **PyHTools** permite operar em três perfis de hardware, dependendo se você utiliza módulos CLI isolados, executa laboratórios de rede/instrumentação Android ou compila executáveis standalone com **PyInstaller / Nuitka**:

| Recurso | 🟢 Mínimo (Módulos CLI Isolados — Web/Rede Básico) | 🟡 Intermediário (MITM de Rede / Sniffer / Lab Android Frida) | 🔵 Recomendado (Suíte Completa + Build PyInstaller / Nuitka) |
| :--- | :--- | :--- | :--- |
| **CPU** | **1 a 2 vCPUs** (`x86_64` / `arm64`) | **2 a 4 vCPUs** (`x86_64` / `arm64`) | **4+ vCPUs** (`x86_64`) |
| **Memória RAM** | **1 GB a 2 GB RAM** | **4 GB RAM** | **8 GB+ RAM** |
| **Armazenamento (SSD)** | **500 MB livres** (Python 3 + dependências pip) | **2 GB livres** (dependências + wordlists + logs de captura) | **5 GB+ SSD** (compilador C p/ Nuitka + PyInstaller + arquivos de lab) |
| **GPU (Opcional)** | Não necessária | Não necessária | Não necessária |
| **Sistema Operacional** | Linux (Kali/Ubuntu/Debian), Windows 10/11 ou Termux (limitado) | Kali Linux ou Ubuntu 22.04/24.04 LTS (recomendado `root` / `sudo`) | Kali Linux (Rolling) ou Ubuntu 24.04 LTS (VM de laboratório isolada) |

#### 📦 Consumo por Componente da Arquitetura
- **CLI Core & Módulos de Rede (`scapy`, `kamene`, ARP/DNS spoofer, sniffer de pacotes, scanner)**: ~40 MB a 150 MB de RAM; requer privilégios `root` / Administrador e acesso a raw sockets / interface de rede em modo promíscuo.
- **Scanners & Crawlers Web (`requests`, `beautifulsoup4`, bruteforcer, spider, crawler)**: ~50 MB a 200 MB de RAM conforme o tamanho das wordlists e concorrência.
- **MITM & Instrumentação Android (`frida-tools`, `pure-python-adb`)**: ~80 MB a 250 MB de RAM (mais dispositivo/emulador ADB conectado).
- **Empacotamento de Executáveis (`pyinstaller` / `nuitka`)**: ~400 MB a 1.5 GB de RAM durante a compilação (`nuitka` requer compilador C local como `gcc` ou MSVC).

#### 🛠️ Dependências de Software
- **Runtime Core**: `Python 3.6+` (recomendado `3.9+`), `pip`, `git`
- **Pacotes Python (`requirements.txt`)**: `scapy >= 2.4.5`, `kamene >= 0.32`, `requests >= 2.25.1`, `beautifulsoup4 >= 4.9.3`, `colorama`, `prettytable`, `pyfiglet`, `psutil`, `pynput`, `frida-tools`, `pure-python-adb`, `pytelegrambotapi`, `zstandard`, `pyinstaller`, `nuitka`
- **Dependências Opcionais por SO**: `netfilterqueue` + `libnetfilter-queue-dev` + `iptables` (recursos Linux MITM/jammer/injector), `wmi` + `Npcap` (Windows), `gcc` / `build-essential` (para compilação via Nuitka)

---

## Installation

### Using pip

- Install main branch using pip

  ```bash
  pip install https://github.com/dmdhrumilmistry/pyhtools.git
  ```

- Install Release from PyPi

  ```bash
  pip install pyhtools
  ```

### Manual Method

- Open terminal

- Install git package

  ```bash
  sudo apt install git python3 -y
  ```

- clone the repository to your machine

  ```bash
  git clone https://github.com/dmdhrumilmistry/pyhtools.git
  ```

- Change directory

  ```bash
  cd pyhtools
  ```

- install requirements

  ```bash
  python3 -m pip install -e .
  ```

## Start PyHTools

- run pyhtools.py

  ```bash
  python3 -m pyhtools
  ```

- to get all the commands use `help`

  ```bash
  pyhtools >> help
  ```

> There may be chances that pyfiglet or kamene will not be installed through requirements.txt, you can install manually using `pip3 install pyfiglet kamene`.  
> If you're using Termux or windows, then use `pip` instead of `pip3`.  
> Few features are only for linux os, hence they might not work on windows and require admin priviliges.

## Package Tools and Features

### Attackers

- `For Networks`
  - Network Scanner
  - Mac changer
  - ARP Spoofing
  - DNS spoofing
  - Downloads Replacer
  - Network Jammer
  - Pkt Sniffer
  - Code Injector
- `For Websites`
  - Login Guesser (Login Bruteforcer)
  - Web Spider
  - Web crawler (detects dirs | subdomains)
  - Web Vulnerablity Scanner
- `For Android`
  - mitm
    - Custom Certificate Pinner

### Detectors

- ARP Spoof Detector

### Malwares/Trojans/Payloads/Ransomwares/Worms

- Email Sender (reporter)
- Downloader
- Wireless Password Harvester
- Credential Harvester
- Keylogger (dlogs)
- Reverse Backdoors
  - TCP
  - HTTP
- Download and Execute
- Telegram Data Harvester
- DMSecRansomware
- Telegram Remote Code Executor
- DirCloner

> **NOTE:** Do not upload/send/report malwares to anti virus services such as `VirusTotal`. This will make program detectable

## How to Package a Evil Files

- [Example Script](./examples/EvilFiles)
- [View How to create a Trojan](./HowTo/Malwares/CreateTrojanPackage.md)
- [Generator Script](./examples/EvilFiles/generatorScript.py)

## Have any Ideas 💡 or issue

- Create an issue
- Fork the repo, update script and create a Pull Request

## Connect With Me

|                                                                                                                       |                                                       Platforms                                                       |                                                                                                                                        |
| :-------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------: |
|       [![GitHub](https://img.shields.io/badge/Github-dmdhrumilmistry-333)](https://github.com/dmdhrumilmistry)        | [![LinkedIn](https://img.shields.io/badge/LinkedIn-Dhrumil%20Mistry-4078c0)](https://linkedin.com/in/dmdhrumilmistry) |             [![Twitter](https://img.shields.io/badge/Twitter-dmdhrumilmistry-4078c0)](https://twitter.com/dmdhrumilmistry)             |
| [![Instagram](https://img.shields.io/badge/Instagram-dmdhrumilmistry-833ab4)](https://instagram.com/dmdhrumilmistry/) |    [![Blog](https://img.shields.io/badge/Blog-Dhrumil%20Mistry-bd2c00)](https://dmdhrumilmistry.github.io/blog)    | [![Youtube](https://img.shields.io/badge/YouTube-Dhrumil%20Mistry-critical)](https://www.youtube.com/channel/UChbjrRvbzgY3BIomUI55XDQ) |
