# Day 2: Python Basics
Today we cover:
* Syntax
* Data Types
* For and While Loops
* Control Flow (If/Else)
* Functions
* Datetime

## Data Types
- Integers - *int*
- Floating-point Numbers - *float* - *NaN* is also float
- Strings - *str*
- Booleans - *bool* - two values: True and False
- Lists - *list*
- Tuples - *tuple*
- Sets - *set*
- Dictionaries - *dict*

## Variables
names given to a memory location (data), we use them to:
- Help organize code
- store specific data
- reuse data over and over
- it can be any data type

## Advanced Data Types
### Lists
- mutable ordered sequence of items.
- Can be indexed, sliced and changed.
- lists can be used for any type of object.
- Can be iterated through

Slice format [***start*:*end*:*step***]
***note**: start index is always inclusive, end index is always exclusive*

*stick to changing a single list value at a time*

**del** list[*index*] - to remove an item at the indicated index position.

You can nest lists within lists.

### Tuple
- immutable objects 
- Similar to a list, but without the functionalities.
- Indexing and splitting similar to lists
- More efficient

Tuples are much faster to execute and iterate over than lists, because they are immutable.

When you use a tuple, you are telling people reading your code "this variable will not change".

Lists are used for *homogeneous* data (i.e. collection of same sort of stuff)

Tuples are used for *heterogeneous* data, where the values are unchanging and represent very different things.

Tuples can also be used as "keys" in dictionary structures, whereas lists cannot, again, due to immutability.

## Dictionary (dict)
- Similar to lists, but can be indexed using "keys" rather than their position.
- "keys" can take on numerous data types (*str int, floats, tuples, lists*)
    * as long as the data type is "hashable"

*note: dictionaries are not 'ordered' data types.

### Sets
Data structure that:
- are unordered, meaning there is no element 0 and no element 1
- values contained are unique - meaning there are no duplicate entries
- sets are made with curly braces {}

![datatypechart](/Unit_1/Day_2/Day_2_Visual_Aids/data_type_chart.png)

### Control Structure (control flow)
- Essential programming concept in any language. allows code to make its own decisions
- executed code *only* if a certain condition is met.
``` 
if [boolean expression]: #starts with if keyword than test condition
    [what to do when the boolean expression evaluates to True]
else:
     [what to do when the boolean expression evaluates to False]

```

**elif** is used for multiple separate conditions and their outcomes. else is used for any outcomes that don't meet specified conditions.

### For Loops (aka. definite iterations)

If all we were able to do with lists, tuples and dictionaries wad store data in them, they would essentially only be useful for organizing out code. We can iterate through these using **for** loops.

```
for [variable] in [iterable data structure]:
    [what you want to do using the current value each iteration]
```

#### Useful Functions

*range(x, y, z)* - used to specify a range from x to y, starting at 0 and excluding the y value, with a step value of z.

## While Loops (aka. indefinite iterations)
Sometimes, we don't want our loop to iterate through the values of some data structure, but instead we want it to execute until some condition is no longer met.

```
while [boolean expression]: 
    [What you want to do each iteration] 
```

## Functions
Parts of code are bound to be reused. A **function** lets us define a chunk of code that takes some *inputs* and returns some *outputs*. As a general rule, if you can give a simple name to what a chunk of code does, you can probably make a function out of it. This is called **modular programming** and it will make your code both easier to write and understand.

*Get in the habit of writing docstrings for your functions, to make it easier on both future you and other programmers who may import your function. Place it at the top of your function, after indenting*

""" Three double quotes create a docstring """

