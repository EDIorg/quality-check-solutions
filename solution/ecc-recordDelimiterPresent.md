# Record delimiter present

### Message:

```
The record delimiter is not present or is not one of the suggested values.
```

### Description:

_The accurate parsing of tabular data requires a record delimiter (new line character) to separate individual records. The absence of a record delimiter can lead to misinterpretation of data and errors in downstream processing._

### Solution:

Metadata editors will often detect the record delimiter automatically from the data table and add it to the EML. If this is the case, then fix the issue in your metadata editor. Alternatively, you can inspect the data table to determine which type of record delimiter is present and manually add it to the EML (see below).

The record delimiter is the character that separates rows. This is often a newline (`\n`), but it can vary depending on the operating system where the file was created. Below is guidance for identifying record delimiters on Linux, Mac, and Windows:

#### 1. **Linux**  
   - **Common Delimiter**: `\n` (newline).  
     Linux-based systems use a single newline character as the record delimiter.  
   - **How to Check**:  
     Open the file in a text editor (e.g., `nano`, `vim`) or use `cat` to display the content. You can also use the `file` command:  
     ```bash
     file your_file.csv
     ```  
     This will output the file type and might indicate the line-ending format.  

#### 2. **Mac**  
   - **Common Delimiter**:  
     - Newer macOS versions (post-OS X) use `\n` (same as Linux).  
     - Older Mac systems (pre-OS X) may use `\r` (carriage return).  
   - **How to Check**:  
     Open the file in a text editor like TextEdit or a command-line tool. To check the exact delimiter, use `od` (octal dump):  
     ```bash
     od -c your_file.csv | head -n 10
     ```  
     Look for `\n` or `\r` at the end of lines.  

#### 3. **Windows**  
   - **Common Delimiter**: `\r\n` (carriage return + newline).  
     Windows uses a combination of `\r` and `\n` to delimit records.  
   - **How to Check**:  
     Open the file in Notepad or a compatible text editor to verify line breaks. On the command line, use `type` to display the file, or check for non-Unix line endings with `findstr`:  
     ```cmd
     findstr "^" your_file.csv
     ```  
     Alternatively, use a tool like Notepad++ or PowerShell:  
     ```powershell
     Get-Content your_file.csv
     ```

#### Cross-Platform Tools  
For a deeper inspection of record delimiters, you can use tools like `hexdump`, `xxd`, or specialized text editors like Visual Studio Code, which display line-ending formats explicitly.  


 

