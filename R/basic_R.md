# R - Easy

## Content:

- [Introduction]()
  - [print() and comments](#print-and-comments)
  - [Variables](#variables)
  - [Data Types](#data-types)
  - [Math]()
  - [Input and Output]()
- [Decision]()
  - [Logical Operators]()
  - [Loops]()
  - [break and next]()
  - [Function]()
- [Data Structures]()
  - [Strings]()
  - [Vectors]()
  - [Lists]()
  - [Matrices]()
  - [DataFrames]()
- [Analyzing Data - basics]()
  - [Data Import]()
  - [Simple Statistics]()
  - [Basic Operations]()
  - [Working with Data]()
  - [Data Grouping]()
- [Visualization]()
  - [Plot function]()
  - [Line Graph]()
  - [Bar Graph]()
  - [Pie Chart]()
  - [Boxplot]()
  - [Histogram]()

## print() and comments

#### Output something:

```R
print("Hello World!")

print("something")
```

#### Comments:

```R
# This is a comment

# This function, print(), will output information

print("information")
```

## Variables

#### Assign variable:

 ```R
 
 # You can choose to use arrow <- to assign a value to a variable
 
 name <- "John"
 
 # Or you can use an equal sign
 
 name = "John"
 
 # Or even a right pointing arrow
 
 "John" -> name
 
 ```
 
 #### Possible variable name:
 
 ![image](https://user-images.githubusercontent.com/82829738/229387680-5b5cfe6e-f684-42d5-9c71-914ac1308026.png)
 
 Image from [Tutorials Point](https://www.tutorialspoint.com/r/r_variables.htm)

 
 ## Data Types

There are six basic common data types:
- character
- numeric
- integer
- complex
- raw
- boolean

```R

# character
chars <- "this is class as character"
print(class(chars)) # -> "character"

# numeric
num <- 105
num2 <- 10.2
print(class(num)) # -> "numeric"
print(class(num2)) # -> "numeric"

# integer
inte <- 5L
print(class(inte)) # -> "integer"

# complex
comp <- 3 + 2i
print(class(inte)) # -> "complex"


# raw
raws <- charToRaw("Hello")
print(class(raws)) # -> "raw"

# boolean
bools_true <- true
bools_false <- false
print(class(bools_true)) # -> "boolean"
print(class(bools_false)) # -> "boolean"
```



