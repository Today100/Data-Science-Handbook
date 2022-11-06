# The Data Processing Pipeline

1. [Acquisition](#Acquisition)
2. [Cleansing/Cleaning](#cleansing--cleaning)
3. [Transformation](#transformation)
4. [Analysis](#analysis)
5. [Storage](#storage)


### Acquisition

- Acquire the data from the source (API, Database, File, etc.)

### Cleansing / Cleaning

- Process of detecting and correcting corrupt or inacurate data
- Removing unnecessary data.
- May not be required if data is ready for analysis.

#### Example:

Data:

> 6.\tThe development shall comply with the requirements of DCCa\x80\x99s Drainage Division as follows \r\n\r\n


Cleaned Data:

> 6. The developemnt shall comply with the requirements of DCC's Drainage Division as follows.


### Transformation

- Process of changing the format or structure of data in preparation for analysis.

#### Example:

Data:

> GoodComps share soared as much as 8.2% on 2021-01-07 after the company announced positive early stage trial results for its vaccine.


Transformed for analysis:
``` PYTHON
["Good Comp", "shares", "soared", "as", "much", "as", "8.2%", "on", "2021-01-07", "after", "the", "company", "announced", "positive", "early-stage", "trial", "results", "for", "its", "vaccine"]
```

### Analysis

- Interpret the raw data.
- Draw conclusion that aren't immediately apparent.

### Storage

- Store the results generated during data analysis process.
