# Internship-Projects-2025


# 🕵️‍♂️ 1. Real-Time Network Packet Sniffer with Alert System

A powerful Python-based packet sniffing tool with live traffic analysis, anomaly detection (port scans, flooding), credential sniffing, DNS logging, and an intuitive GUI built using Tkinter and ttkbootstrap.

![Screenshot 2025-06-27 155909](https://github.com/user-attachments/assets/0c54e133-7172-48e2-9020-5397d48cee46)


---

## 📌 Features

- 📡 **Real-Time Packet Sniffing** with Scapy
- 📊 **Live Dashboard** with protocol & port usage graphs
- ⚠️ **Anomaly Detection** for:
  - Port Scans (10+ ports in 10s)
  - Flooding (100+ packets in 10s)
- 🧠 **Credential Sniffing** (toggleable)
- 🌐 **DNS Query Logging**
- 🗃️ **SQLite Logging** for packets, DNS, and credentials
- 📨 **Email Alerts** via SMTP
- 🔐 **Settings Panel** to enable/disable sniffing features
- 🧾 **Search & Export Logs** (CSV format)
- 🖥️ **Modern GUI** with ttkbootstrap

---

## 🧰 Tech Stack

- Python 3.10+
- [Scapy](https://scapy.net/)
- Tkinter + ttkbootstrap
- Matplotlib
- SQLite
- smtplib + dotenv

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/network-sniffer-alert-system.git
cd network-sniffer-alert-system
```

2. Install Dependencies

```bash
pip install -r requirements.txt
```

3. Setup .env for Email Alerts

```bash
EMAIL_SENDER=youremail@example.com
EMAIL_PASSWORD=yourapppassword
EMAIL_RECEIVER=admin@example.com
SMTP_SERVER=smtp.gmail.com
SMTP_PORT=587
```
⚠️ Use App Passwords for Gmail or provider-specific SMTP.

4. Run the App

```bash
python main.py
```

## 📁 Project Structure

```bash
network-sniffer-alert-system/
├── app/
│   ├── gui.py                 # GUI and dashboard logic
│   ├── sniffer.py             # Packet sniffing & detection engine
│   └── utils/                 # Optional helper modules
├── main.py                    # Entry point for GUI
├── .env                       # Email credentials (excluded in .gitignore)
├── requirements.txt
└── README.md
```

## 🛡️ Future Improvements
- IP blocking / firewall integration
- Slack or webhook alerts
- GeoIP mapping
- Advanced rule-based anomaly engine
- CLI-only mode (optional)

## 🧪 Testing
### Basic functionality can be tested using:

```bash
ping google.com
nslookup example.com
curl -d "username=admin&password=1234" http://test.local/login
```

## 📦 Packaging
### Use PyInstaller to create a standalone .exe:

```bash
pyinstaller --onefile --windowed main.py
```

## 📄 License
### MIT License © 2025 [Pradeep Behera]

### 🙋‍♂️ Contribution
```bash
Pull requests and issues welcome! Please fork the repo and submit PRs for improvements or bug fixes.
```

# 🔐 2. Secure File Storage System with AES-256 Encryption

A robust Python application to encrypt and decrypt files locally using AES-256 encryption. It offers both a Command-Line Interface (CLI) and a user-friendly PyQt5-based GUI. Supports metadata logging, tamper detection, bulk file handling, and secure logging.

---

## 📌 Features

- 🔒 AES-256 (Fernet-based) encryption & decryption
- 🧾 Metadata logging (file name, timestamp, SHA-256 hash)
- 🛡️ File integrity verification (tampering detection)
- 📦 CLI & GUI (PyQt5) support
- 📂 Bulk file encryption & decryption
- 🧠 Filename obfuscation with UUID + SHA256
- 📋 Export metadata and decrypted file paths to CSV
- 📊 Drag & drop GUI with progress bar
- 🚫 Overwrite prevention with `--force` option
- 🪵 Secure logging to `secure_vault.log`

---

## 🛠 Tools & Libraries

- Python 3.11+
- PyQt5 (GUI)
- cryptography (AES-256 encryption)
- hashlib, base64
- argparse (CLI)
- JSON & CSV (metadata handling)
- FPDF (PDF report generation)

---

## 🗂️ Project Structure

```bash
Secure_File_Storage_System_with_AES/
├── main.py # CLI logic
├── gui_launcher.py # PyQt5 GUI entry point
├── app/
│ ├── crypto_utils.py # Encryption/Decryption logic
│ ├── metadata_utils.py # Metadata handling
│ └── gui.py # PyQt5 GUI logic
├── tests/
│ └── test_main.py # Pytest unit tests
├── metadata.json # Stored metadata (auto-generated)
├── secure_vault.log # Log file (auto-generated)
```

---

## 🚀 Getting Started

### 1. Install Requirements

```bash
pip install -r requirements.txt
```

### 2. Run GUI

```bash
python gui_launcher.py
```

### 3. Run CLI
### Encrypt a file:

```bash
python main.py encrypt sample.txt --password yourpassword
```

### Decrypt a file:

```bash
python main.py decrypt encrypted_files/abc123.enc --password yourpassword
```

### Optional Flags:

--force: Overwrite output files if they exist

--output-dir path/to/folder: Set output folder for decrypted files

### ✅ Run Tests

```bash
pytest tests/test_main.py
```

## 📤 Export Features
- Export metadata to CSV via GUI
- Log all encryption/decryption attempts in secure_vault.log
- Export decrypted file paths

## 🔐 Security Notes
- Uses PBKDF2 with SHA-256 for secure key derivation
- Salt is randomly generated for every encryption
- Obfuscated filenames via SHA-256 + timestamp
- File integrity is verified using SHA-256 hash

## 📦 Build Executable (Optional)
### Use PyInstaller to package:

```bash
pyinstaller main.py --name SecureFileVault --onefile
```

## 📃 License
MIT License – Use freely with credit.

# 🔐 3. Password Strength Analyzer & Wordlist Generator

A dual-purpose security tool for:

- **Analyzing password strength**
- **Generating targeted password wordlists**

This tool is useful for red teamers, penetration testers, or anyone who wants to test password resilience or create realistic wordlists for audit.

---

## 📦 Features

### 🔍 Password Analyzer
- Uses [`zxcvbn`](https://github.com/dropbox/zxcvbn) to assess password strength
- Crack time estimation & feedback
- Password preview toggle (GUI)

### 🧠 Custom Wordlist Generator
- Inputs: name, birth date, pet name, favorite book, car/bike, etc.
- Adds leetspeak, case flips, year suffixes, common patterns
- Outputs `.txt` files under `wordlists/` folder
- File auto-naming with timestamp + unique ID
- Prompts for overwrite & auto-opens file (GUI)

### 🖼️ GUI with Tkinter
- Tabs for password analysis and wordlist generation
- Toggle to show/hide password input
- User-friendly experience

---

## 🚀 Getting Started

### 🧰 Requirements

Create virtual environment:
```bash
venv\Scripts\activate
```
Install dependencies:
```bash
pip install -r requirements.txt
```

### ▶️ Run (CLI)
```bash
python main.py
```
### 🖱️ Run (GUI)
```bash
python app/gui_main.py
```

### 📁 Project Structure
```bash
password_strength_analyzer/
├── app/
│   ├── analyzer.py
│   ├── generator.py
│   ├── ui_cli.py
│   └── gui_main.py
├── wordlists/
├── main.py
├── requirements.txt
```

### 🧾 License
MIT License © 2025 Pradeep Behera
```bash
Feel free to download.
```

# 🕵️‍♂️ 4. Steganography Tool — Hide and Extract Text or Files in Images

A Python-based steganography tool with a Tkinter GUI that allows you to securely hide and extract messages (with optional encryption) in image files. Supports drag-and-drop, encryption using Fernet (PBKDF2-derived key), and JPEG-to-PNG conversion to preserve pixel integrity.

---

## 📦 Features

- 🔒 **Password-based Encryption** (Fernet/AES via PBKDF2)
- 🖼️ **Supports PNG, JPG, JPEG, BMP** (JPEGs are auto-converted to PNG)
- 🐭 **Drag & Drop Image Interface**
- 📐 **Image Metadata Preview** (size, dimensions)
- 🧠 **Automatic Detection of Encrypted vs Plain Text**
- 📁 **Save, Clear, Extract Functions**
- ✅ **Integrity Check for Hidden Messages**
- 🧪 **Test Scripts Included for Automation**
- 📦 **Export as Executable (.exe)**

💡 Credits
Developed with ❤️ using Python, NumPy, and Pillow

Cryptography powered by Fernet

GUI built using TkinterDnD2

🤝 Contributing
Pull requests are welcome! For major changes, please open an issue first.

## 🚀 Getting Started
### 🔧 Installation

Clone the repo:

```bash
git clone https://github.com/yourusername/steganography-tool.git
cd steganography-tool
```

Install dependencies:

```bash
pip install -r requirements.txt
```             
Note: If you get errors for numpy, Pillow, or cryptography, install them individually:
```bash
pip install numpy pillow cryptography tkinterdnd2
```

### ▶️ Run the App

```bash
python main.py    
```
The GUI will launch. Drag and drop an image, type a message, and click "Hide Message".

🛠️ Project Structure
```bash
steganography_tool/
│
├── gui/
│   └── app.py               # Main Tkinter GUI
│
├── stegano/
│   ├── embed.py             # Embeds text/file in image using LSB
│   ├── extract.py           # Extracts text/file from image
│
├── tests/
│   └── V2_test_steganography.py  # CLI test script
│
├── main.py                  # Entry point
├── requirements.txt         # Dependencies
└── README.md
```

🔐 How It Works

Converts message to bits and embeds LSB into image.

Optionally encrypts message using Fernet + password.

Detects and decodes messages starting with:

ENC:: → Encrypted

TXT:: → Plaintext

JPEGs are automatically converted to PNG before embedding.

🧪 Testing
Run test script to embed/extract sample messages:
```bash
python V2_test_steganography.py
```

📦 Build as .exe (Windows)
Install PyInstaller:
```bash
pip install pyinstaller
```
Build:
```bash
pyinstaller --onefile --windowed main.py
```
Add a custom icon with --icon=icon.ico

🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first.

💡 Credits

Developed with ❤️ using Python, NumPy, and Pillow

Cryptography powered by Fernet

GUI built using TkinterDnD2

