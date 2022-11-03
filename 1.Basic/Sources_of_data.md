# Sources of Data
- [API](#api)
- [Web Pages](#web-pages)
- [Database](#database)
- [Files](#files)

## API

- A software intermediary that enables two applications to interact with each other.
- Usually return results with formats such as JSON, XML, or CSV.

Choosing API:
  - Functionality
    - Understand precise requirements.
  - Cost
    - Many APIs allow user to use a so-called *developer key*. Usually free but with certain limitations.
  - Stability
    - Ones that has reliability
  - Documentation
    - How to use the API

## Web Pages

- Web scraping.
- Python libraries for web scraping:
  - Requests
    - Fetches the source code of the page.
  - BeautifulSoup
    - Creates a *parse tree* for the page.

Fragment of parse tree:

```HTML
[<td title="03/01/2020 00:00:00"><a href="Download.aspx?ID=630751" id="lnkDownload630751" target="_blank">03/01/2020</a></td>
<td title="03/01/2020 00:00:00"><a href="Download.aspx?ID=630753" id="lnkDownload630753" target="_blank">03/01/2020</a></td>
<td title="03/01/2020 00:00:00"><a href="Download.aspx?ID=630755" id="lnkDownload630755" target="_blank">03/01/2020</a></td>]
```
Transformed:

```
[
{'Document_Reference' : '630751', 'Document_Date' : '03/01/2020', 'link' : 'http://www.dummy.com/Download.aspx?ID=630751'}
{'Document_Reference' : '630753', 'Document_Date' : '03/01/2020', 'link' : 'http://www.dummy.com/Download.aspx?ID=630753'}
{'Document_Reference' : '630755', 'Document_Date' : '03/01/2020', 'link' : 'http://www.dummy.com/Download.aspx?ID=630755'}
]
```
## Database

- A structure that proviides a mechanism to efficiently store, access, and manipulate structured data.
- Using Structured Query Language (SQL)

```SQL
SELECT first_name, last_name FROM employees WHERE department = 'IT' and title = 'programmer'
```

NoSQL databases:
 - Use flexible data models.
 - Store large volumes of unstructured data using *key-value* method.

|key|value|
|---|-----|
|...|...|
|26|GoodComp shares a soared as much as 8.2% on 2021-01-07 after the company announced...|

## Files

- May contain structured, semistructured, and unstructured data.
- Use corresponding library based on the format of data (CSV, JSON, XML, etc.)

```
dat= 'Jul 19 10:30:37'
host='sm1-prt-highw157'
syslogtag='%SYS-1-CPURISINGTHRESHOLD'
msg=' Threshold: Total CPU Utilization(Total/Intr): 17%/1%, Top 3 processes(Pid/Util): 85/9%, 146/4%, 80/1%'
```



