# fido-key-converter

## ℹ️ About
**key-convert** is a utility to convert a FIDO2 _public_ key credential for use with Yubico's pam-u2f module. Specifically, the tool connects to a YubiKey to obtain any public key used for SSH (Relying Party ID == ´ssh:´) and then converts and outputs one or more public key identities in a format acceptable to *pam-u2f*. This enables the user to use a single device-bound passkey (resident key) for both remote access to Linux (ssh), as well as Linux interactive use (pam-u2f). In doing so, the solution also enables administrators to more easily remote onboard end-users for Linux host access. To simplify adoption and use, key-convert is provides as a single file binary for **Windows**, **Linux** and **macOS**.

## ℹ️ About
**key-convert** is a utility that converts a FIDO2 _public_ key credential for use with Yubico’s **pam-u2f** module. It specifically retrieves SSH public keys stored on a YubiKey (where the Relying Party ID is ´ssh:´) and converts them into a format compatible with pam-u2f.

This allows users to leverage a single device-bound passkey (resident key) for both:
✅ Remote access to Linux via SSH
✅ Interactive authentication on Linux via pam-u2f

By enabling this dual functionality, key-convert simplifies remote onboarding for administrators, making it easier to grant Linux host access to end users.
To streamline adoption, key-convert is distributed as a single-file binary for **Windows**, **Linux**, and **macOS**.

## ⚠️ Disclaimer
The binaries provided herein is made available on an "as-is" basis, without any warranties or representations, whether express, implied, or statutory, including but not limited to implied warranties of merchantability, fitness for a particular purpose, or non-infringement.

## 💻 Prerequisites
_Use of key-convert requires the following prerequisites be met:_
- YubiKey with support for Credential Management (all current YubiKeys)

## 💾 Installation
No installation is required (just run download and run the binary as shown below), however you _may_ need to exempt or whitelist the executable in your antivirus client (likely due to heuristics detection of the C compiler / build tool used to create the utility).

## 📖 Usage

**Convert public key interactively:**
_If you just run the utility it will prompt for PIN when required:_

```bash
convert-key
```

**Convert public key with PIN as an argument**
_You can provide PIN as an argument using either `-p` or `--pin` (shown):_

```bash
convert-key --pin 1234
```

## 📖 Roadmap
Possible improvements includes:
- Convert any public key by RP
- Inclusion of GUI framework


### 🥷🏻 Contributing
You can help by getting involved in the project, _or_ by donating (any amount!).   
Donations will support costs such as domain registration and code signing (planned).

[![Donate](https://www.paypalobjects.com/en_US/i/btn/btn_donate_LG.gif)](https://www.paypal.com/donate/?business=RXAPDEYENCPXS&no_recurring=1&item_name=Help+cover+costs+of+the+SWJM+blog+and+app+code+signing%2C+supporting+a+more+secure+future+for+all.&currency_code=USD)

## 📜 Release History
* YYYY.MM.DD `vX.X.X`
