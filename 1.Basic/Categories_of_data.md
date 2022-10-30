# Types of Data

- [Unstructured](#unstructured-data)
- [Structured](#structured-data)
- [Semistructured](#semistructured-data)
- [Time Series](#time-series-data)

## Unstructured Data

- Data with no predefined organizational system or schema.
- Most widespread form of data
- Ex. Images, Videos, Audios, Natural language texts.
- May contain important information
- Could be extract and convert to structured or semistructured data through transformation and analysis steps.
  - Image recognition tools first convert the collection of pixels within an image into a dataset of a predefined format and then analyze this data to identify content in the iamge.

#### Example:

> GoodComp shares soared as much as 8.2% on 2021-01-07 after the company announced positive early-stage trial results for its vaccine.


- Information isn't organized with a predefined schema.
- Information randomly scattered within the statement.
- Rewritable in any number of ways.


> Following the January 7, 2021, release of positive results from its vaccine trial, which is still in its early stages, shares in GoodComp rose by 8.2%.


## Structured Data

- Has predefined format of how data is organized.
- Usually stored in a repository like a relational databse or .csv file.
- Data fed into such a repository is called a ***record***
- Information is orgniazed in ***fields***
- records of the same structure are logically grouped in a container called a ***table***
- Two types of Structured Data:
  - Numerical data
    - Expresses information in numerical form.
    - Allowing the perform of mathematical operations.
  - Categorical data
    - Can be categorized on the basis of similar characteristics.
    - Can sometimes take on numerical values.
      - ZIP codes, Phone numbers, etc.

#### Example one:

Format:
```
Company: ABC
Date: 	 yyyy-mm-dd
Stock: 	 nnnnn
```
Apply Format to Data:
```
Company: GoodComp
Date: 	 2021-01-07
Stock: 	 +8.2%
```
Store in Database: 
|Company|Date|Stock|
|:-------:|:----:|:-----:|
|GoodComp|2021-01-07|+8.2%|

#### Example two:

Format:
```
Company: ABC
Date: 	 yyyy-mm-dd
Product: DEF
Stage:   XYZ
```
Apply Format to Data:
```
Company: GoodComp
Date: 	 2021-01-07
Product: Vaccine
Stage:   Early-stage trial
```
Store in Database: 
|Company|Date|Product|Stage|
|:-------:|:----:|:-----:|:---:|
|GoodComp|2021-01-07|Vaccine|Early-stage trial|


## Semistructured Data


## Time Series Data
