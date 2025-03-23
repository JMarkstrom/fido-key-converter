# fido-key-converter

## ℹ️ About
**key-convert** is a utility that converts a FIDO2 _public_ key credential for use with Yubico’s **pam-u2f** module. It specifically retrieves SSH public keys stored on a YubiKey (where the Relying Party ID is `ssh:`) and converts them into a format compatible with pam-u2f.   

This allows users to leverage a single device-bound passkey (resident key) for both:   

✅ Remote access to Linux via SSH   
✅ Interactive authentication on Linux via pam-u2f   

By enabling this dual functionality, **key-convert** simplifies remote onboarding for administrators, making it easier to grant Linux host access to end users. To streamline adoption, key-convert is distributed as a single-file binary for **Windows**, **Linux**, and **macOS**.

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
Example output:   

```none
Found 1 credential(s) for RP (ssh:):

:*,YAOzTPcgn3XVjFOlxjwopXgrv9BcaNEqa15BJLw6tJIevbwM54rTTLuS2x7mUz4a3JNHJIVBV3/Mbf/tSvJXBA==,es256,+presence+pin
```
**NOTE**: For instructions on integration of the converted public key into **pam-u2f** see [![this](https://swjm.blog/fido2-security-key-sign-in-on-linux-3f9f9fd629d7)
 guide.


## 📖 Roadmap
Possible improvements includes:
- Convert any public key by RP
- Inclusion of GUI framework


### 🥷🏻 Contributing
You can help by getting involved in the project, _or_ by donating (any amount!).   
Donations will support costs such as domain registration and code signing (planned).

[![Donate](https://www.paypalobjects.com/en_US/i/btn/btn_donate_LG.gif)](https://www.paypal.com/donate/?business=RXAPDEYENCPXS&no_recurring=1&item_name=Help+cover+costs+of+the+SWJM+blog+and+app+code+signing%2C+supporting+a+more+secure+future+for+all.&currency_code=USD)

## 📜 Release History
* 2025.03.22 `v0.0.1`
