# Integrity Checksum Presence

### Message:

```
Warning/Error: A physical/authentication element is present and specifies a method attribute with a value of MD5 or SHA-1
```

### Description:

_Integrity checks help ensure that **no data loss or corruption** occurred during file transfer from the author to the repository. Verifying checksums allows you to confirm that the file remains unchanged._

### Solution:

If you encounter this issue, double-check the **MD5 checksum** value for the data entities in your data package to ensure accuracy.

#### Generating an MD5 Checksum on Different Operating Systems:

##### **Windows (Command Prompt & PowerShell)**
- **Using Command Prompt:**
  1. Open **Command Prompt** (`Win + R`, type `cmd`, and press Enter).
  2. Run the following command:
     ```
     certutil -hashfile "C:\path\to\file" MD5
     ```
  3. The MD5 checksum will be displayed.

- **Using PowerShell:**
  1. Open **PowerShell**.
  2. Run:
     ```
     Get-FileHash "C:\path\to\file" -Algorithm MD5
     ```
  3. The MD5 checksum will be shown.

##### **Mac (Terminal)**
- Open **Terminal** (`Cmd + Space`, type `Terminal`, and press Enter).
- Run the following command:
  ```
  md5 "path/to/file"
  ```
- The output will display the MD5 checksum.

##### **Linux (Terminal)**
- Open **Terminal**.
- Run the following command:
  ```
  md5sum "path/to/file"
  ```
- The MD5 checksum will be displayed.

  

