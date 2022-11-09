# Sets

- A *set* iis an unordered collection of unique items.
- No duplicate items in a *set*.

```Python
{"Bob", "Amy", "George"}
```

## Removing Duplicateds from Sequences

- Since all value in a set must be unique, sets are really useful to remove duplicate items from a list or a tuple.

```Python

lst = ["Bob", "George", "Bob", "Emily", "Alice", "Mona", "Emily"]

# Converts list to set to get rid of duplicate items, and then convert back to list.
lst = list(set(lst))

print(lst)
# ['George', 'Alice', 'Emily', 'Mona', 'Bob']

```
- Drawback of the appraoch in the previouse codeblock is that it does not preserve the initial order of elements.
- In order to get a ordered list, **sorted()** could be used.

```Python
lst = ["Bob", "George", "Bob", "Emily", "Alice", "Mona", "Emily"]

# Converts list to set to get rid of duplicate items, and then convert back to list.
lst = list(sorted(set(lst), key=lst.index))

print(lst)
# ['Bob', 'George', 'Emily', 'Alice', 'Mona']

```

## Performing Common Set Operations

- Set objects come with methods for performing common math operations on sequences, like *unions* and *intersections*.

#### intersection()

```Python

num1 = {1, 3, 5, 7, 9}
num2 = {2, 4, 3, 5, 0}

intersections = num1.intersection(num2)

print(intersections)
# {3, 5}


```
#### union()

```Python

num1 = {1, 3, 5, 7, 9}
num2 = {2, 4, 3, 5, 0}

unionss = num1.union(num2)

print(unions)
# {0, 1, 2, 3, 4, 5, 7, 9}

```
