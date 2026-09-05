<div align="center">
  <h1>GuestRegister</h1>
  <p>Free Fire guest account registration and account activation utility</p>

  <a href="https://github.com/siambhau/GuestRegister">
    <img src="https://img.shields.io/badge/Repository-GitHub-111827?style=for-the-badge&logo=github&logoColor=white" alt="GitHub Repository">
  </a>
  <a href="#quick-start">
    <img src="https://img.shields.io/badge/Setup-Quick_Start-16a34a?style=for-the-badge" alt="Quick Start">
  </a>
</div>

<br>

## Overview

GuestRegister is a terminal-based utility for creating Free Fire guest account records with a simple interactive workflow.

The project is designed for Android devices running Termux. It asks for a few basic settings, connects to the required services, and saves the result as a JSON file.

## Features

- Simple Free Fire guest account generator
- JSON output for generated account records

<div align="center">
  <h2>VPN REQUIRED</h2>
  <p><strong>VPN must be enabled before generating accounts.</strong><br>
  Do not start the account generation process without an active VPN connection.</p>
</div>

## Tools included

| Option | Purpose | Input | Output |
| --- | --- | --- | --- |
| `1. Guest Register` | Creates new Free Fire guest account records | Account name, region, quantity, filename | `<filename>.json` |
| `2. Account Activator` | Currently unavailable | Do not use this option | Not supported at this time |

## Requirements

- Android with Termux recommended
- Python 3.9 or newer
- Git
- Active internet connection
- Permission to write to Android shared storage
- A valid approval from the project administrator

For Android storage access, run this once in Termux if required:

```bash
termux-setup-storage
```

## Quick start

Clone the repository and enter the project directory:

```bash
git clone https://github.com/siambhau/GuestRegister
cd GuestRegister
```

Install the required Python packages:

```bash
pip install -r requirements.txt
```

Make the launcher executable and start the tool:

```bash
chmod +x GuestRegister
./GuestRegister
```

The launcher starts `GuestRegister.py` and keeps the requested `./GuestRegister` command available.

## Guest Register

Choose `1. Guest Register` from the menu and enter the account name, region, account quantity, output filename, and save folder. Review the summary and enter `Y` to start.

The result is saved in the current directory and also copied to:

```text
/storage/emulated/0/BhauXGuestRegister/<filename>.json
```

The output is a formatted JSON file containing the generated account records.

## Account Activation status

The `Account Activator` option is currently not working and should not be used. Use only the `Guest Register` option until the activation workflow is fixed and officially enabled again.

## Supported region codes

The available region codes are:

```text
ME  IND  ID  VN  TH  BD  PK  TW  EUROPE
RU  NA  SAC  BR  SG  US  CIS
```

Use the region code expected by the target service. The default region is `BD`.

## Configuration

Default values are defined in `GuestRegister.py`:

```python
CONFIG = {
    "TOTAL_ACCOUNTS": 10000,
    "ACCOUNT_NAME": "SiamBhau",
    "FILENAME": "freefire_accounts",
    "THREAD_COUNT": 400,
    "REGION": "BD",
}
```

Most values can be changed interactively when the program starts.

## Troubleshooting

### Permission denied when starting

Run:

```bash
chmod +x GuestRegister
```

Then start the tool again:

```bash
./GuestRegister
```

### Python module is missing

Install the project dependencies:

```bash
pip install -r requirements.txt
```

If your Termux installation uses `pip3`, run:

```bash
pip3 install -r requirements.txt
```

### Telegram does not open

This is expected on environments without Android intent support. Open Telegram manually, visit `@SiamBhau`, and send the generated access key.

### Key is still pending

The approval status is checked automatically every five seconds. Keep the tool open after sending the key, or stop it with `Ctrl+C` and run it again later.

## Responsible use

Use this project only with accounts, devices, and network access that you are authorized to use. Follow Garena and Free Fire terms, local laws, and any applicable platform rules. Do not use the tool for spam, fraud, unauthorized access, or any activity that harms other users or services.

This project communicates with third-party services over the network. Service availability, response formats, rate limits, and account eligibility may change without notice. No guarantee is made that every requested operation will succeed.

## Contact

For access approval and project-related questions, contact:

<div align="center">
  <a href="https://t.me/SiamBhau">
    <img src="https://img.shields.io/badge/Telegram-@SiamBhau-229ED9?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram @SiamBhau">
  </a>
</div>

## License

Unless a license file is added to this repository, all rights are reserved by the project owner. Do not redistribute, repackage, or commercially use this project without permission.
