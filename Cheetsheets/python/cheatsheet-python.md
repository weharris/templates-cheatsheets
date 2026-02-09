# Python cheatsheet


## Data types
```python
my_integer_var = 10
print(type(my_integer_var))  # <class 'int'>

my_float_var = 4.50
print(type(my_float_var))  # <class 'float'>

my_string_var = 'hello'
print(type(my_string_var))  # <class 'str'>

my_boolean_var = True
print(type(my_boolean_var))  # <class 'bool'>

my_set_var = {7, 5, 8}
print(type(my_set_var))  # <class 'set'>

my_dictionary_var = {'name': 'Alice', 'age': 25}
print(type(my_dictionary_var))  # <class 'dict'>

my_tuple_var = (7, 5, 8)
print(type(my_tuple_var))  # <class 'tuple'>

my_range_var = range(5)
print(type(my_range_var))  # <class 'range'>

my_list = [22, 'Hello world', 3.14, True]
print(type(my_list)) # <class 'list'>

my_none_var = None
print(type(my_none_var))  # <class 'NoneType'>
```

## String methods

```python
my_string = "Hello, World!"
print(my_string.upper())  # HELLO, WORLD!
print(my_string.lower())  # hello, world!
print(my_string.split())  # ['Hello,', 'World!']
print(my_string.replace('Hello', 'Goodbye'))  # Goodbye, World!
print(my_string.find('World'))  # 7
print(my_string.index('World'))  # 7
print(my_string.title())  # Hello, World!
```