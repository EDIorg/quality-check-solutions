# Integrity Checksum

### Message:

```
Warning/Error: Compare the metadata checksum for an entity to the checksum of the downloaded entity.
```

### Description:

_The **MD5 checksum** allows for an integrity check to ensure that no data corruption has occurred during transmission. This helps verify that the file uploaded by the author is identical to the one stored in the repository._

### Solution:

Many metadata editors can automatically generate and include this checksum. However, if you need to determine it manually, you can do so using the following methods:

#### Determining MD5 Checksum:

- **Windows**:  
  1. Open **Command Prompt** (Press `Win + R`, type `cmd`, and hit Enter).  
  2. Run the following command:  
     ```
     certutil -hashfile "C:\path\to\file" MD5
     ```
  3. The MD5 checksum will be displayed.

- **Mac**:  
  1. Open **Terminal** (Press `Command + Space`, type `Terminal`, and hit Enter).  
  2. Run the following command:  
     ```
     md5 "path/to/file"
     ```
  3. The MD5 checksum will be displayed.

- **Linux**:  
  1. Open **Terminal**.  
  2. Run the following command:  
     ```
     md5sum "path/to/file"
     ```
  3. The MD5 checksum will be displayed.
