# Number Of Records Presence

### Message:

```
Warning/Error: Is the numberOfRecords element present?
```

### Description:

_Ensuring consistency between the **number of records** listed in the metadata and the **actual number of records in the file** helps confirm that **no data corruption or loss** occurred during file transfer. This check is especially important when **processing large datasets** to ensure integrity and completeness._

### Solution:

To address this issue, **verify the number of records** within the data entity and ensure it matches the value recorded in the metadata.

#### Detecting the Number of Records in a File  

##### **Windows (Command Prompt & PowerShell)**  
- **Using Command Prompt:**  
  1. Open **Command Prompt** (`Win + R`, type `cmd`, and press Enter).  
  2. Run the following command:  
     ```
     find /c /v "" "C:\path\to\file.csv"
     ```
  3. The output will display the number of lines (records) in the file.

- **Using PowerShell:**  
  1. Open **PowerShell**.  
  2. Run the following command:  
     ```
     (Get-Content "C:\path\to\file.csv").Count
     ```
  3. The number of lines in the file will be displayed.


##### **Mac & Linux (Terminal)**  
- **Using `wc` (Word Count Command):**  
  1. Open **Terminal**.  
  2. Run the following command:  
     ```
     wc -l "path/to/file.csv"
     ```
  3. The output will display the number of lines (records) in the file.

- **Using `awk` (For Skipping Headers if Needed):**  
  - If the first row is a **header** and should not be counted as a record, use:  
    ```
    awk 'NR>1 {count++} END {print count}' path/to/file.csv
    ```
  - This will **skip the header** and count only data records.

- **Using `sed` to Count Records (Excluding Header):**
  ```
  sed 1d path/to/file.csv | wc -l
  ```
  - This removes the first line (header) before counting.
  
