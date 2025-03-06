# Number Of Records

### Message:

```
Warning/Error: Number of records in metadata matches number of rows loaded.
```

### Description:

_Knowing the number of records in a data file can be useful for verifying integrity similar to an MD5 checksum, but also useful in file read operations. [Other reasons?]._

### Solution:

Many metadata editors can automatically detect and include this information. However, if you need to determine it manually, you can do so using the following methods:

[Add methods for determining the number of records, or rows in a data table file, from Windows, mac, and linux platforms]



### Description:

_Knowing the number of records (rows) in a data file helps verify **data integrity**, similar to an MD5 checksum. It also ensures that file read operations process the expected number of records, preventing issues like **truncated data** or **incomplete uploads**. Additionally, record counts can be useful for **quality control, tracking changes**, and **debugging issues** when working with large datasets._

### Solution:

Many metadata editors can automatically detect and include the record count. However, if you need to determine it manually, you can use the following methods:

#### Determining the Number of Records (Rows):

- **Windows (Command Prompt using PowerShell)**:  
  1. Open **Command Prompt** (Press `Win + R`, type `cmd`, and hit Enter).  
  2. Run the following command:  
     ```
     powershell "(Get-Content 'C:\path\to\file.csv').Length"
     ```
  3. The output displays the number of rows in the file.

- **Mac & Linux (Terminal)**:  
1. Open **Terminal**.  
2. Run the following command:  
   ```
   wc -l "path/to/file.csv"
   ```
3. The output displays the number of rows in the file.  

*For files with headers:*  
- If the first line is a header and should not be counted as a record.

