# Date Format Matches

### Message:

```
Warning/Error: Date format in metadata matches data
```


### Description:

_Dates should be consistently formatted and should match the **formatString** specified in the metadata. Inconsistencies in date formats can lead to **parsing errors**, **data loss**, and **misinterpretation** of temporal information._

### Solution:

Ensure that all date and time values in your dataset follow a **consistent format** that aligns with the metadata description. The [preferred formats](https://github.com/EDIorg/ECC/blob/master/practices/dateTimeFormatString/dateTimeFormatString_list.csv) should be explicitly defined in the metadata.

#### Reformatting Date and Time Values:

##### **Python (pandas)**
If your dataset is in **CSV** or a similar tabular format, you can use the `pandas` library to reformat dates:

```python
import pandas as pd

# Load data
df = pd.read_csv("data.csv")

# Convert and reformat the date column
df["date_column"] = pd.to_datetime(df["date_column"], format="%Y-%m-%d")  # Adjust format as needed

# Save the cleaned data
df.to_csv("cleaned_data.csv", index=False)
```

Common datetime format strings:

"%Y-%m-%d" → 2024-03-06

"%Y-%m-%d %H:%M:%S" → 2024-03-06 14:30:00

#### **R (lubridate)**
In R, you can use the lubridate package to ensure consistent date formats:

```R
library(lubridate)

# Load dataset
df <- read.csv("data.csv")

# Convert and format the date column
df$date_column <- ymd(df$date_column)  # Adjust function (mdy(), dmy(), etc.) as needed

# Save cleaned data
write.csv(df, "cleaned_data.csv", row.names = FALSE)
```

#### **Microsoft Excel**
If using Excel, follow these steps to standardize date formats:

1. Select the column containing dates.
2. Click on Format Cells (Ctrl + 1 or Cmd + 1 on Mac).
3. Choose Custom or Date, then select or define the preferred format (e.g., YYYY-MM-DD).
4. Export the file as CSV to maintain the format.

⚠️ Important:
Once you have reformatted your dates in Excel and exported them as CSV, avoid re-importing the file into Excel without specifying the correct format, as Excel may automatically change the dates back to your system's default settings.
