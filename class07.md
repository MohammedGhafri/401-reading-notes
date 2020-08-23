# Python Scope

## globals

* globals() is a built-in function that returns a reference to the current global scope or namespace dictionary.
* call globals() in a given module, then you’ll get a dictionary containing all the names that you’ve defined in that module

```
[name for name in globals() if name.startswith('__')]
['__name__', '__doc__', '__package__',..., '__annotations__', '__builtins__']

```

* WE  can iterate through it through it using these traditional methods:

1. .keys()
1. .values()
1. .items()


## locals   

This function updates and returns a dictionary that holds a copy of the current state of the local Python scope or namespace.

```
def func(arg):
    var = 100
    print(locals())
    another = 200
```
Call the function : `func(300)`

```
{'var': 100, 'arg': 300}
```


## summery :

1. Take advantage of Python scope to avoid or minimize bugs related to name collision
2. Make good use of global and local names across your programs to improve code maintainability
3. Use a coherent strategy to access, modify, or update names across all your Python code

