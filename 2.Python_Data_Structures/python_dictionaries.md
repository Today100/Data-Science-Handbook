# Dictionaries

- Muutable, unordered collections of *key-value pairs*.
- Each *key* is a unique name that identifies an item of data, the *value*.

```Python
{"name" : "Bob", "student_num" : 123456, "age" : 18}
```

## A List of Dictionaries

```Python

students = [
{"name" : "Bob", "student_num" : 123456, "age" : 18},
{"name" : "Saline", "student_num" : 234567, "age" : 18},
{"name" : "Amy", "student_num" : 345678, "age" : 19},
{"name" : "Sarah", "student_num" : 456789, "age" : 18},
{"name" : "Emily", "student_num" : 567890, "age" : 17}
]

print(students[0]["name"])
# "Bob"

print(students[2]["age"])
# 19

print(students[-1]["student_num"])
# 567890
```

## Adding to a Dictionary with setdefault()

- provides a convenient way to add new data to a dictionary.
- takes a key-value pair as its parameter.
- If specified key already exists, the method returns the current value of that key.
- If specified key doesn't exists, setdefault() inserts the key with the specified value.

```Python

student = {
  "name" : "Bob", 
  "student_num" : 123456, 
  "age" : 18
}

print(student.setdefault("name", "Ashika"))
# "Bob"

print(student.setdefault("sex", "male"))
# "male"

print(student)
# student = {
#   "name" : "Bob", 
#   "student_num" : 123456, 
#   "age" : 18,
#   "sex" : "male"
# }

```

#### Practical Example: Using setdefault() to count the appearence of words in a given sentences.

```Python

txt = '''Python is one of the most promising programming languages today. Due to the simplicity of Python syntax, many researchers and scientists prefer Python over many other languages.'''

txt = txt.replace('.', '').replace(',', '')

lst = txt.split()

print(lst)
# ['Python', 'is', 'one', 'of', 'the', 'most', 'promising', 'programming', 'languages', 'today', 'Due', 'to', 'the', 'simplicity', 'of', 'Python', 'syntax', 'many', 'researchers', 'and', 'scientists', 'prefer', 'Python', 'over', 'many', 'other', 'languages']

dct = {}
for w in lst:
  c = dct.setdefault(w, 0)
  dct[w] += 1
  
dct_sorted = dict(sorted(dct.items(), key=lambda x: x[1], reverse=True))

print(dct_sorted)
# {'Python': 3, 'of': 2, 'the': 2, 'languages': 2, 'many': 2, 'is': 1, 'one': 1, 'most': 1, 'promising': 1, 'programming': 1, 'today': 1, 'Due': 1, 'to': 1, 'simplicity': 1, 'syntax': 1, 'researchers': 1, 'and': 1, 'scientists': 1, 'prefer': 1, 'over': 1, 'other': 1}

```

## Loading JSON into a Dictionary

```PYTHON

import json

# Dump dictionary to a json file
with open("file.json", "w") as outfile:
  json.dump(data, outfile)

# Get json data from file as dictionary
with open("file.json",) as fp:
  data = json.load(fp)

```

