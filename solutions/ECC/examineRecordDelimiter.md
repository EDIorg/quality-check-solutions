# Examine Record Delimiter

### Message:

```
Warning/Error: Data are examined and possible record delimiters are displayed
```

### Description:

_Ensuring **consistent record delimiters** within a data entity (e.g., a file) allows the data to be correctly **parsed and read** by different applications. Inconsistent delimiters can lead to **misalignment of records, data corruption, or failed imports** into processing tools._

### Solution:

To resolve this issue, try one of the following approaches:

- **Regenerate or re-export the data** using the original program it was created in, ensuring that a consistent delimiter is applied.
- **Manually correct inconsistencies** in record delimiters using built-in tools or text editors.

#### Ensuring Consistent Record Delimiters on Different Operating Systems:

##### **Windows (Using Notepad++ or PowerShell)**
- **Using Notepad++:**
  1. Open the file in **Notepad++**.
  2. Click **View > Show Symbol > Show End of Line** to check for inconsistent delimiters.
  3. Convert all delimiters by selecting **Edit > EOL Conversion**, then choose a standard format (e.g., **Unix (LF)** or **Windows (CRLF)**).
  4. Save the file.

- **Using PowerShell:**
  1. Open **PowerShell** and run:
     ```
     Get-Content "C:\path\to\file" | Set-Content -NoNewline "C:\path\to\cleaned_file"
     ```
  2. This removes inconsistent newlines and ensures uniform line endings.

##### **Mac & Linux (Using Terminal)**
- **Using `sed` to Convert to Unix (LF) Format:**
  1. Open **Terminal**.
  2. Run:
     ```
     sed -i 's/\r$//' path/to/file
     ```
  3. This ensures all lines end with a **Unix-style LF delimiter**.

- **Using `dos2unix` for Windows to Unix Conversion:**
  1. If your file was created in Windows and has **CRLF** endings, install `dos2unix` (if not already installed).
  2. Run:
     ```
     dos2unix path/to/file
     ```
  3. This converts all line endings to **Unix LF** format.

- **Using `file` and `tr` to Detect & Fix Mixed Delimiters:**
  1. Check the current delimiter format:
     ```
     file path/to/file
     ```
  2. If mixed delimiters are detected, convert them to Unix format:
     ```
     tr -d '\r' < path/to/file > cleaned_file
     ```
