# Entity Size Presence

### Message:

```
Warning/Error: Check for presence of an entity size element
```

### Description:

_Including the entity size (data file size) helps users understand how large the data objects are before downloading them. This information is useful for estimating **storage requirements** and **network transfer times**._

### Solution:

Ensure that each entity includes an **entity size value in bytes**.

Many metadata editors can automatically detect and include this information. However, if you need to determine the file size manually, you can do so using the following methods:

#### Determining File Size in Bytes:

- **Windows**:  
  1. Right-click the file and select **Properties**.  
  2. The **Size** field displays the file size in bytes.  

  *Command-line method:*  
  - Open **Command Prompt** and run:  
    ```
    dir "C:\path\to\file"
    ```
  - The size is displayed in bytes.

- **Mac**:  
  1. Right-click (or Control + click) the file and select **Get Info**.  
  2. The file size is listed under **Size** in bytes.  

  *Terminal method:*  
  - Open **Terminal** and run:  
    ```
    ls -l "path/to/file"
    ```
  - The file size (in bytes) is shown in the output.

- **Linux**:  
  - Open **Terminal** and run:  
    ```
    ls -l "path/to/file"
    ```
  - The file size in bytes is shown in the output.  

  *Alternative method:*  
  - Run:  
    ```
    stat -c %s "path/to/file"
    ```
  - This will return only the file size in bytes.

