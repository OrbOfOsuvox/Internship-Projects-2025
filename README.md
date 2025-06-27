# Internship-Projects-2025


# 🕵️‍♂️ Steganography Tool — Hide and Extract Text or Files in Images

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


# 🔐 Password Strength Analyzer & Wordlist Generator

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
