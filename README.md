🪐 EVE Layout Copier v3.8 (EVE Lacop)

**EVE Layout Copier (EVE Lacop)** is a lightweight, portable utility designed for **EVE Online** players who manage multiple accounts.  
It allows you to **clone window layouts**, **save configurations between profiles**, and **manage multiple character setups** with a few clicks.

---

## ⚙️ Features
- Clone one character’s layout to multiple others.
- Save source layouts into any destination profile folder.
- Manage profiles (create, delete, or switch instantly).
- Automatic backup before overwriting files.
- Displays character names and portraits via EVE API.
- Multilingual interface: English, Portuguese, Chinese, Russian, French, Spanish, and German.
- Portable — no installation required.

---

## 🚀 How to Use
1. Launch `EVE_Layout_Copier_v3.8.exe`.
2. Select **one origin character** (source layout).
3. Select **one or more destination characters**.
4. Click **Execute Copy** to duplicate the layout.
5. Use **Save Origin Layout** to copy layouts into another profile folder.
6. Manage profiles via `+` and `−` buttons (e.g., create `settings_Mining`).
7. All backups are automatically stored in the folder `eve layout backup`.

OR

https://youtu.be/AMZPskW9Ok0

---

## 🧩 Requirements
- Windows 10/11  
- Python 3.10+ (only if running from `.py`)  
- Internet connection (for EVE portraits & character names)  

---

## 🔧 Building from Source
If you want to compile your own `.exe`, install **PyInstaller** and run the following command inside the project folder:

```bash
pip install pyinstaller
pyinstaller --onefile --noconsole --icon="icon.ico" --clean --name="EVE_Layout_Copier_v3.8" eve_layout_copier_v3.8.py
