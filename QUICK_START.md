# Quick Start Guide

## 🚀 Get Started in 2 Minutes

### Step 1: Prepare Your File
Save your Room EQ settings as a `.txt` file. Example:
```
Filter  1: ON  PK       Fc   55.30 Hz  Gain  -11.1 dB  Q  2.000
Filter  2: ON  PK       Fc  135.50 Hz  Gain   -8.5 dB  Q  2.000
```

### Step 2: Run the Converter
Open Terminal/Command Prompt and run:

```bash
python3 convert_eq_to_fabfilter.py "your_eq_file.txt"
```

**Example:**
```bash
python3 convert_eq_to_fabfilter.py "EQ 23 Aug.txt"
```

### Step 3: Use Your Preset
The script creates a `.fxml` file. Now:

**Option A - Drag & Drop (Easiest)**
- Open FabFilter Pro-Q 4
- Drag the `.fxml` file into the preset browser
- ✅ Done!

**Option B - Move to Presets Folder**
- Copy the `.fxml` file
- Paste it in your FabFilter presets folder (see paths below)
- Restart FabFilter
- ✅ Done!

---

## 📁 FabFilter Presets Folder Location

### Windows
```
C:\Users\[YourUsername]\AppData\Roaming\FabFilter\Pro-Q 4\Presets\
```

### Mac
```
~/Library/Application Support/FabFilter/Pro-Q 4/Presets/
```

### Linux
```
~/.config/FabFilter/Pro-Q 4/Presets/
```

---

## 📝 Input File Format

Your file must contain filter lines like this:
```
Filter  1: ON  PK       Fc   55.30 Hz  Gain  -11.1 dB  Q  2.000
```

Key parts:
- `Filter X:` - Filter number
- `ON` - Must be ON (not OFF)
- `PK` - Filter type (PK, LP, HP, LS, HS)
- `Fc XXX.XX Hz` - Center frequency
- `Gain XX.X dB` - Gain in decibels
- `Q X.XXX` - Q factor

---

## ✨ Examples

### Convert with default name:
```bash
python3 convert_eq_to_fabfilter.py "EQ 23 Aug.txt"
# Creates: Custom_EQ.fxml
```

### Convert with custom name:
```bash
python3 convert_eq_to_fabfilter.py "EQ 23 Aug.txt" "Studio Setup"
# Creates: Studio_Setup.fxml
```

---

## ❓ Common Issues

### "python: command not found"
Use `python3` instead of `python`

### "File not found"
- Make sure the file is in the same folder as the script
- Include quotes around filenames with spaces

### No filters found
- Check your file format matches the examples
- Make sure filters start with "Filter" and contain "ON"

---

## 🎉 That's It!

Your EQ preset is now ready to use in FabFilter Pro-Q 4!

Need help? Check the full README.md for more details.
