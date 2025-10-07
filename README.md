# 🛡️ PAN Data Validation and Cleaning Utility

A **robust command-line utility** for cleaning, validating, and reporting on Permanent Account Numbers (PAN) from an Excel dataset.  
It applies **strict validation logic**, cleans inconsistencies, and produces a **comprehensive summary** of valid, invalid, and excluded records.

---

## ✨ Features

### 📂 Interactive File Handling
- Prompts the user for both the **input Excel file** and **desired output filename**.  
- Automatically handles file loading and saving.

### 🧹 Comprehensive Data Cleaning
- Trims whitespace and converts all PANs to **uppercase**.  
- Removes **missing, empty, or placeholder** PAN entries.  
- **De-duplicates** records, keeping the first occurrence.  

### ✅ Strict PAN Validation Rules
Each PAN is validated against multiple structural and logical rules:

| Rule | Description |
|------|--------------|
| **Length Check** | Must be exactly **10 characters** long |
| **Format Check** | Must match the pattern **`AAAAA9999A`** (5 letters, 4 digits, 1 letter) |
| **Sequential Letters Prevention** | Rejects sequences like `ABCDE` |
| **Sequential Digits Prevention** | Rejects numeric runs like `1234` |
| **Repetition Check** | Rejects adjacent repetition like `AABB` |

### 📊 Detailed Reporting
Generates an Excel report with two structured sheets:
1. **PAN Validations** — Shows each record and its validation status (`Valid` / `Invalid`).
2. **Summary** — Displays overall counts:
   - Total Records  
   - Valid PANs  
   - Invalid PANs  
   - Excluded Records  

### 💡 Formatted Console Output
- Displays a **color-coded summary** of the validation process directly in the terminal for instant insight.

---

## 🚀 Getting Started

### Prerequisites
- Python **3.x**
- Required Python libraries:
  ```bash
  pip install pandas openpyxl

## 🧠 Tech Highlights

- Language: Python
- Libraries: pandas, openpyxl
- Output: Excel report + Terminal summary


