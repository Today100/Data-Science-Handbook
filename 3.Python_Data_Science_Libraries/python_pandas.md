# Pandas

- The de facto standard for data-oriented Python applications.
- Includes two data structures: *Series* (1D) and *DataFrame* (2D)

## Installation

```console
$ pip install pandas
```

## Pandas Series

- 1D labeled array.
- Elements in a Series are labeled with integers according to their position by default.
- Can specify custom labels.
- Labels need not be unique, but must be of a hashable type (such as integers, floats, strings or tuples).

- Elements can be any type, but it is better if all elements is the same type.


### Creating a Series

```Python

import pandas as pd

data = ["Bob", "Jerry", "Annie"]
names = pd.Series(data)

print(names)

# 0      Bob
# 1    Jerry
# 2    Annie
# dtype: object
```
- Customized: 
```Python

import pandas as pd

data = ["Bob", "Jerry", "Annie"]
names = pd.Series(data, index=[1001, 1002, 1003])

print(names)

# 1001      Bob
# 1002    Jerry
# 1003    Annie
# dtype: object
```

### Accessing Data in a Series

```Python
print(names[1003])
# Annie

print(names.loc[1002])
# Jerry

print(names.iloc[0])
# Bob

print(names.loc[1001:1002])
# 1001 Bob
# 1002 Jerry

print(names[0:2])
# 1001 Bob
# 1002 Jerry
```

### Combining Series into a DataFrame

- Multiple Series can be combined to form a DataFrame.

```Python

email_data = ["bob.hello", "jerry.wow", "annie.cool"]

emails = pd.Series(email_data, index=[1001, 1002, 1003], name="emails")

names.name = "names"

df = pd.concat([names, emails], axis=1)

print(df)
#       names      emails
# 1001    Bob   bob.hello
# 1002  Jerry   jerry.wow
# 1003  Annie  annie.cool


```

## pandas DataFrame

![finallpandas](https://user-images.githubusercontent.com/82829738/202919884-59a07a38-e28e-446b-a834-9c7db4b5472f.png)



### Creating a padas DataFrame

- From lists
```Python

import pandas as pd

student_id_data = [135, 246, 357, 468, 579]
names_data = ["Bobby", "Alice", "Amy", "Mary", "Huston"]
math_grade_data = [90, 78, 88, 95, 0]
eng_grade_data = [80, 90, 92, 67, 100]

data = {"id" : student_id_data, 
        "name" : names_data,
        "math_grade" : math_grade_data,
        "english_grade": eng_grade_data}
        
grade_df = pd.DataFrame(data)
grade_df = df.set_index("id")

print(grade_df)
```
![image](https://user-images.githubusercontent.com/82829738/202920549-0cc391ff-7bb2-4927-9783-bbec21d0dbf0.png)

- From JSON

```Python
import json
import pandas as pd

data = [
{"Empno":9001, "Salary": 3000},
{"Empno":9002, "Salary": 2800},
{"Empno":9003, "Salary": 2500},
]


json_data = json.dumps(data)
salary = pd.read_json(json_data)
salary = salary.set_index("Empno")
print(salary)
```
![image](https://user-images.githubusercontent.com/82829738/202920243-a8d28be7-ba43-49d1-a740-333c0dc9a9e1.png)

Code: https://onecompiler.com/python/3ypj7b7xc

### Combining DataFrames

- DataFrames support database-style join operations through two methods: **merge()** and **join()**

```Python

data = [
  [135, "m"],
  [246, "f"],
  [579, "m"],
  [357, "f"],
  [468, "f"]
  
]

gender_df = pd.DataFrame(data, columns=["id", "gender"])
gender_df = gender_df.set_index("id")

student_info = df.join(gender_df)
print(student_info)
```
![image](https://user-images.githubusercontent.com/82829738/202921032-9c798b45-76f3-4b02-a6ae-70f2e025a70c.png)
