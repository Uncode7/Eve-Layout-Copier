Here you go—short, GitHub-ready and all in English.

---

# EVE Layout Copier – v3.9 (EVE Lacop)

## What’s new in v3.9

* **Profiles UX**

  * Profile dropdown shows all `settings_*` folders (hides `cache`).
  * **Auto-format** profile names when creating (e.g., “alts mining” → `settings_alts_mining`) to match EVE Launcher requirements.
  * **Delete selected layouts** in Destination (no need to wipe the whole folder).
  * Live labels showing the **current folder** for Origin/Destination.
* **Safer copy**

  * Atomic writes + optional **Backup before** (timestamped “eve layout backup” next to the app).
  * **Dry-run** (test mode) with tooltip guidance.
* **Clarity & speed**

  * **Character portraits & names** on both Origin and Destination (caching with refresh).
  * Tooltips translated (multi-language UI) and cleaner character tooltips:

    ```
    Your Char Name
    core_char_xxx.dat
    core_user_xxx.dat
    ```
  * Origin pane narrower, Destination wider; scrollbars thicker.
  * Messageboxes/dialogs now use the **custom app icon** (no more Tk feather).
* **Small QoL**

  * “Mark/Unmark All” in Destination.
  * Help panel updated and localized.
  * Throttled writes to reduce corruption when cloning many alts at once.

---

## Quick Start (User)

1. **Origin**: pick one character to clone *from*.
2. **Destination**: pick one or more characters to clone *to*.
3. (Optional) Choose/Manage a **Profile** (`settings_Default` or another `settings_*` folder).
4. (Recommended) Keep **Backup before** ON. Keep **Dry-run** OFF for real copying.
5. Click **Execute copy**.

> **Tip:** If your character layout does not appear, run the game once to (re)generate `core_char_*.dat` and `core_user_*.dat` in the selected profile folder.

---

## Save layouts into another profile

* Select **one or more** origins in the Origin pane.
* Choose the **Destination profile** in the right dropdown.
* Click **Save origin layout into destination profile** (creates/overwrites those files in that profile).

---

## Delete selected layouts (Destination)

* Select one or more Destination characters.
* Click **Delete selected layouts**.
* Confirms and deletes only those selected files inside the current Destination profile.

---

## Profiles & EVE Launcher notes

* Profiles must be named like `settings_*` (no spaces; use underscores).
* The app **auto-formats** your input (e.g., “alts de mineração” → `settings_alts_de_mineração`).
* To switch profiles in-game, set it in the **EVE Launcher** before launching:

  * Click the account → **Settings** → choose profile (or create a **Launch Group**).

---

## Safety features

* **Backups:** `eve layout backup/<YYYY-MM-DD_HH-MM-SS>/…` beside the EXE.
* **Atomic writes:** prevents partial/corrupted saves.
* **Dry-run:** safe test mode (does not modify files).

---

## Build (Windows)

> Requires Python + pip + PyInstaller. Run in the folder with the `.py` and `icon.ico`.

**PowerShell:**

```powershell
python -m PyInstaller `
  --onefile `
  --windowed `
  --clean `
  --noconfirm `
  --name "EVE_Layout_Copier_v3.9" `
  --icon "icon.ico" `
  --add-data "icon.ico;." `
  eve_layout_copier_v3.9.py
```

**CMD:**

```bat
python -m PyInstaller --onefile --windowed --clean --noconfirm ^
  --name "EVE_Layout_Copier_v3.9" ^
  --icon "icon.ico" ^
  --add-data "icon.ico:." ^
  eve_layout_copier_v3.9.py
```

The executable will be in `dist\EVE_Layout_Copier_v3.9.exe`.

---

## Donate

If you liked it, please send an ISK donation to **“Plunder Skol”** 💙 s2
[https://zkillboard.com/character/2116662655](https://zkillboard.com/character/2116662655)

---

## Known tips

* If portraits don’t show immediately, click **Refresh**.
* Close the EXE before rebuilding (prevents “Access denied” errors).
* Keep **Backup before** ON when testing new profiles.
