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
