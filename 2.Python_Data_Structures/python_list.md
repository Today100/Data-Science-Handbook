# List

- An ordered collection of objects.
- Elements are separated by commas.
- Enclosed in square brackets.

```PYTHON
[2, 4, 7]
["Bob", "John", "Will"]
```

## Creating a List

- Place a sequence of elements inside square brackets and assign the sequence to a variable name.

```Python
regions = ["Asia", "America", "Europe"]
names = []
```

## Using Common List Object Methods

- Most common list object methods:
  - append()
  - index()
  - insert()
  - count()

### append()

```Python
names = []

names.append("Bob")
names.append("Henry")
names.append("Selina")
names.append("Amy")
names.append("Alice")

print(names)
# ["Bob", "Henry", "Selina", "Amy", "Alice"]

#Using indicies:

print(names[0])
# "Bob"

print(names[1])
# "Henry"

print(names[-1])
# "Alice"

print(names[-2])
# "Amy"
```

### index() and insert()

index()
- Find the index of a given object in the list.

insert()
- Insert the given value into a given index.

```Python

names = ["Bob", "Henry", "Selina", "Amy", "Alice"]

print(names.index("Bob"))
# 0

print( names.index("Amy"))
# 3

names.insert(0, "Bobby")
print(names)
# ["Bobby", "Henry", "Selina", "Amy", "Alice"]

names.insert(2, "Shelly")
print(names)
# ["Bobby", "Henry", "Shelly", "Amy", "Alice"]


```

### count()

- Count the number of appearence of a given value in a list.

```Python
names = ["Bob", "Bob", "Selina", "Amy", "Alice"]

print(names.count("Bob"))
# 2

print(names.count("Amy"))
# 1

```

## Using Slice Notation


```Python
names = ["Bob", "Henry", "Selina", "Amy", "Alice"]

print(names[0:3])
# ["Bob", "Henry", "Selina"]

print(names[3:])
# ["Amy", "Alice"]

print(names[:-1])
# ["Bob", "Henry", "Selina", "Amy"]


names[0] = "Bobby"

print(names)
# ["Bobby", "Henry", "Selina", "Amy", "Alice"]

names[5:] = ["Emily", "Joseph"]

print(names)
# ["Bobby", "Henry", "Selina", "Amy", "Alice", "Emily", "Joseph"]
```

## Using a List as Queue

- A *queue* is an abstract data type that can be implemented using the list data structure.
- One end of a queue is always used to insert items (*enqueue*), and the other is used to remove them (*dequeue*), thus following the *first-in, first-out (FIFO)* methology.


```
from collections import deque

to_dos = ["Pay bills", "Tidy up", "Walk the dog", "Go to the pharmacy", "Cook dinner"]
queue = deque(to_dos)

queue.append("Wash the car")

print(queue.popleft(), "- Done!")
# "Pay bills - Done!"

new_to_dos = list(queue)

print(new_to_dos)
# ["Tidy up", "Walk the dog", "Go to the pharmacy", "Cook dinner", "Wash the car"]

```

## Using a List as a Stack

- A *stack* is an abstract data structure that you can organize on top of a list.
- Implements the *last-in, first-out (LIFO)* methodology.

```Python
to_dos = ["Pay bills", "Tidy up", "Walk the dog", "Go to the pharmacy", "Cook dinner"]
stack = []
for task in to_dos:
  stack.append(task)

while stack:
  print(stack.pop(), '- Done!')
print("\nThe stack is empty")

# Cook dinner - Done!
# Go to the pharmacy - Done!
# Walk the dog - Done!
# Tidy up - Done!
# Pay bills - Done!

# The stack is empty

```

## Using Lists and Stacks for Natural Language Processing

**PASS**

## Making Improvements with List Comprehensions

### List Comprehensions:

```Python

num = [1, 5, 8, 9, 2, 10, 31, 0, 3, 4]

larger_num = [n for n in num if n > 7]

print(larger_num)
# [8, 9, 10, 31]

```
