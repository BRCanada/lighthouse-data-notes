# Collections
Functions, modules and packages are all constructs in Python that promote code modularization.
## Module
Nothing more than a .py script that can be called in another .py script. A file containing Python definitions and statements which helps to implement a set of functions. Modules are imported from other modules using the *import* command. 

### Python's in-built modules
You can reference a full list using [Python Module Index](https://docs.python.org/3/py-modindex.html)

#### dir()
A built in function used to find out which functions are implemented in each module. Returns a sorted list of strings.
After locating our desired function in the module, we can read more about it using the **help** function, inside the python interpreter:
```
help(<built-in function>)
```

### Packages
A collection of related modules stacked up together. Numpy and Scipy, the core machine learning packages, are made up of a collection of hundreds of modules. We used alot of these packages in the onboarding lessons.

## Collections Module
Built-in Python module that implements specialized container datatypes. These provide alternatives to Python's general purpose containers such as dict, list, set, and tuple.
some useful data structures in this module are:

### namedtuple()

Data stored in a plain tuple can only be accessed through indexes. We can't give names to individual elements stored in a tuple. 
**namedtuple** is a function that allows for tuples with named fields, and can be seen as an extension on the standard tuple data type.
They assign meaning to each position in a tuple. Each object stored in these can be accessed through a unique identifyer, freeing us from having to remember indexes.

```
    from collections import namedtuple
    fruit = namedtuple('fruit','number variety color')
    guava = fruit(number=2,variety='HoneyCrisp',color='green')
    apple = fruit(number=5,variety='Granny Smith',color='red')
```

Namedtuples are also a memory-efficient option when defining an immutable class in Python.

### Counter
A dict subclass which helps to count hashable objects. Elements are stored as dictionary keys while the object counts are stored as the value. 

Counters support three methods beyond those typically available for all dictionaries:

* **elements()**
    Returns a count of each element, and if an element's count is less than one, it is ignored.
* **most_common([n])**
    Returns a list of most common elements, with their counts. The number of elements is specified with *n*. If none is specified, it returns the count of all elements.

![counterpatterns](/Unit_1/Day_2/Day_2_Visual_Aids/Counter_patterns.png)

* **defaultdict()**
    Dictionaries are efficient ways to store data for later retrieval having an unordered set of *key:value* pairs.
    Where a dictionary will return an error if you call an object that is not in it already, **defaultdict** will create any items that you try to access (provided they do not exist yet). 

* **OrderedDict**
    a dictionary subclass that remembers the order in which keys were first inserted. When iterated over, the ordered dictionary returns items in the order they were first added. 