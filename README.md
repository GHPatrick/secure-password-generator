# Secure Password Generator

This Python script generates secure, memorable passwords using a combination of real English words, random digits, and special characters. It also evaluates the strength of each password using the `passwordmeter` library. 

---

## File Overview

- **main.py** – Core script that generates and evaluates secure passwords.
- **words.txt** – Word list used for generating phrases for passwords. 

---

## Features

- Combines random **English words**, **digits**, and **special characters**
- Tests password **strength** with `passwordmeter`
- Automatically downloads a **public English word list** if `words.txt` is missing
- Fully **customizable**: adjust word count, digit count, and symbol count
- Simple, self-contained script. 

---

## Use Case

This script is ideal for cybersecurity professionals, sysadmins, or developers who need:
- To generate strong, easy-to-remember passwords for end-users
- A lightweight, offline password generator
- A customizable tool for penetration testing toolkits or security automation

---

## Getting Started

### Requirements

- Python 3.x
- Internet access (on first run only, to download `words.txt`)

### Installation

```bash
git clone https://github.com/GHPatrick/secure-password-generator.git
cd secure-password-generator
pip install passwordmeter
```

## Running the Script

```bash
python3 main.py
```
Sample output:

```makefile
Password: PineappleRiver8361@
Strength: 0.87423
```

## Customization 

Inside `main.py`, you can change the default password format by editing the parameters of the `create_password()` function:

```python
create_password(num_words=3, num_number=2, num_special=2)
```
Or modify directly inside the `main()` function for consistent usage. 

## How it Works
- Checks if `words.txt` exists locally. If not, downloads it from a trusted GitHub source.
- Randomly selects a defined number of English words, capitalizes them, and appends random digits and special characters.
- Evaluates the password's strength using entropy-based scoring from `passwordmeter`.

## Why this Project?
This project showcases:
- Python scripting for cybersecurity applications
- Secure password generation techniques
- Real-world automation and user-centric security tools
