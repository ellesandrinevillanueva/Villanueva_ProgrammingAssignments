# ECE-2112-PA-1
#### Villanueva, Elle Sandrine P. | 2ECE-C
This repository contains Programming Assignment 1 for the course Advanced Computer Programming, S.Y. 2026-2027. The objectives are to: 

1. Utilize basic Python functions, operators, and string operations;
2. Manipulate strings using recognized string methods;
3. Manipulate lists through sequence unpacking; and
4. Construct user-defined Python functions that return a specified result.
## A. Word Rotation Problem

This problem requires a function that moves the first character to the end while keeping the capitalization of all characters.

The function uses slicing to extract the character at index 0, retain characters from index 1 onwards, and place the character at index 0 at the end.

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

The second problem asks for a function named make_username() that accepts two strings: first name and last name. It should convert all letters to lowercase, remove all spaces from both strings, and join them with a period.

``make_username(first name, last_name)`` accepts two strings. To store these, ``new_firstname`` and ``new_lastname`` were created.

A ``for`` loop checked whether the characters were uppercase using ``.isupper()``. If tagged in uppercase, ``.swapcase()`` will change it before adding it to ``new_firstname``. If the character is already in lowercase, it will be returned as is. The same ``for`` loop was applied to ``new_lastname``.

``.replace()`` was used to remove spaces with an empty string.

Lastly, the username is returned with a period joining them.

The completed code is shown below.
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

The third task is to create a function named ``swap_bookends()`` that accepts a list with at least two elements and unpacks it into three variables: first, middle, and last. It should return a new list with the first and last elements exchanged, while the middle remains in its original position.

``first, *middle, last = items`` separates the list in three parts.

The returned output switched the last element and the first element.

The final function is:

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

August 28, 2026 - Added description
