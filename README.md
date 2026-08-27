# ECE-2112-PA-1
#### Villanueva, Elle Sandrine P. | 2ECE-C | Date Submitted: August 27, 2026
### Objective

## A. Word Rotation Problem
This function uses slicing to retain characters from index 1, extract index 0, and place it at the end.

* `rotate_word()` - a user-defined function that prints out the second and the following characters, placing the first character in the end.

```
def rotate_word(text):
  print(text[1:]+text[0])
```

**Examples:**

``rotate_word("python")``

ythonp

``rotate_word("Code")``

odeC

``rotate_word("logic")``

ogicl

## B. Username Builder Problem
```
def make_username(first_name, last_name):
    new_firstname = ""
    new_lastname = ""

    for x in first_name:
        if x.isupper():
            new_firstname += x.swapcase()
        else:
            new_firstname += x
    for x in last_name:
        if x.isupper():
            new_lastname += x.swapcase()
        else:
            new_lastname += x

    new_firstname = new_firstname.replace(" ", "")
    new_lastname = new_lastname.replace(" ", "")

    return new_firstname + "." + new_lastname
```

**Examples:**

``make_username("Ada","Lovelace")``

'ada.lovelace'

``make_username("Alan","Turing")``

'alan.turing'

``make_username("Ana Maria","De Leon")``

'anamaria.deleon'

## C. Booked Swap Problem

```
def swap_bookends(items):
    first, *middle, last = items
    return [last] + middle + [first]
```

**Examples:**

``swap_bookends([1, 2, 3, 4, 5, 6])``

[6, 2, 3, 4, 5, 1]

``swap_bookends(["red", "green", "blue"])``

['blue', 'green', 'red']

``swap_bookends([8,3])``

[3, 8]


**README File Version History**

August 27, 2026 - Initial submission
