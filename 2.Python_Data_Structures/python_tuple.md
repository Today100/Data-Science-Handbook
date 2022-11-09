# Tuples

- A tuple is an ordered collection of objects.
- Tuples are **imutable** (cannot be changed after creation)

```Python
("Bob", "Jenny", "Ellen")
```

## A List of Tuples

- It is common to nest Python data structures inside each other.

```Python
[("8:00, "Pay bills"), ("8:30", "Tidy up"), ("9:30", "Walk the dog"), ("10:00", "Go to the pharmacy"), ("10:30", "Cook dinner")]
```

```Python

tasks = ["Pay bills", "Tidy up", "Walk the dog", "Go to the pharmacy", "Cook dinner"]

time = ["8:00", "8:30", "9:30", "10"00", "10:30"]

schedual = [(tm, task) for tm, task in zip(time, tasks)]

print(schedual)
# [("8:00, "Pay bills"), ("8:30", "Tidy up"), ("9:30", "Walk the dog"), ("10:00", "Go to the pharmacy"), ("10:30", "Cook dinner")]

print(schedual[1][0])
# "8:30"
```

#### Immutabiligy:

```Python

schedual = [("8:00, "Pay bills"), ("8:30", "Tidy up"), ("9:30", "Walk the dog"), ("10:00", "Go to the pharmacy"), ("10:30", "Cook dinner")]
schedual[1][0] = "9:10"

# TypeError: "tuple" object does not support item assignment.
```
