# Python OOP


## Create a virtual env

```shell
python3 -m venv <path_to_name>
deactivate
source <path_to_name>/bin/activate
```

### Install packages in v_env

- Use the following code to install the required modules in the virtual env.
- [requirements.txt](./requirements.txt)
- `python3 -m pip install -r requirements.txt`
- Execute python commands from shell.
    - `python3 -c "import Cars"`

## Packages

- A collection of relatable modules.

### Create a package

- Create a folder with the desired name. Example, Cards.
- Create a python file `__init__.py` and enter the code inside this file.
- The package name is the folder name.

### Application packages

- Two types of packages:
    - Source packages (sdist)
    - Distribution packages (bdist)

- Packaging a python app requires following:
    - Python modules or packages
    - [pyproject.toml file](./packaging/pyproject.toml)
    - A build front-end
    - A build back-end

## Modules

- Standard modules in python; sys, os, math, collections, random, 

- collections.py
    - namedtupes, deque, orderedDict, defaultdict, UserString, ChainMap, COunter, UserDict, UserList

- random.py
    - used to generate random data, but it's a psuedo randomness, better not use in crucial randomness is needed.[]


## Comprehensions

- A shorthand style of syntax that can be replaced for for_loops with a sinngle line of code.
- List, dictionary and Sets.
- [comprehensions.py](./comprehensions.py)


## Exceptions

- Python raises exceptions when there are excpetions to the expected code-flow. There are two main exceptions:
    - Syntax Errors
    - Runtime Exceptions
- Ex: `SyntaxError`, `ValueError`, `FileNotFoundError` etc...
- Exceptions are python objects.
- When there's an error and we can use `raise` keyword to raise and `Exception`.
\
&nbsp;
- Exceptions are raised when the code cannot recover from a situation and don't know how to proceed, we can use exceptions to recover the code and proceed with the flow.
- Can be used for autohealing.
\
&nbsp;
- Can use multiple excaptions in a single try-except block.
- Or can consolidate into a single exception and return a single output.
- In exception handling you can catch multiple exceptions by puting them in a tuple.
    - `except (ValueError, ZeroDivisionError)`
- In exceptions we can bound a name to the exception raised and use it later in the code.
- Custom exceptions can be created by creating a new class and inheriting the `Exception` class.
- [exceptions.py](./exceptions.py)
\
&nbsp;
- Re-raising exceptions, raising more specific exceptions, and exception chaining helps to prevent ineffective handlers.
- It's not always clear how to handle an exception; however they should almost never be uused to silence exceptions.
- If a handler cannot effectively handle the exceptional condition it should be re-raised.
- Exceptions that remain unhandled all the way back through the call stack indicate ineffective or missing handlers.
- Not all exceptions require the original exception to be chained.
- Passing a None value to from keyword causes the original exception to be suppressed.
- [reraise_exceptions.py](./reraise_exceptions.py)
\
&nbsp;
- The class hierarchy for built-in [exceptions](https://docs.python.org/3/library/exceptions.html#exceptions-heirarchy).
- The [BaseException](https://docs.python.org/3/library/exceptions.html#eBaseException).
- Exception handling in 3rd-party applications using heirarchy, [Example](https://github.com/pallets/flask/blob/36af821edf741562cdcb6c60d63f23fa9a1d8776/src/flask/cli.py#L122).


## Classes

- The `self` attribute is bound to the instance of the that class.
- What ever in that first spot will be bound to the the current object from the python runtime.
- Two types of attributes.
    - Class attributes.
    - Instance attributes.
\
&nbsp;
- In a class no need to define the attributes beforehand (class attributes), just put them inside the `__init__` method and it can be used in the other methods. This is called instance attribute defining.
- Instance attributes can be defined inside methods, but better to initialze them when the object was created, these attributes can used as global class attributes.
- `__init__` method is reffered to as a constructor.
\
&nbsp;
- Two types of methods.
    - Class methods: Linked to the type and have access to class attributes and other class methods.
    - Instance methods: Linked to an object instance and have access to both class and instance attributes and methods.
