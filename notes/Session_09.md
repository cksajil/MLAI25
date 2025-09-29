# Control Flow
## IF
This checks a condition, and if it's true, the indented code block under it will be executed.
```python
if True:
    print("Inside if block")
```

[![Python IF](https://img.youtube.com/vi/nY4XQDsZzFY/0.jpg)](https://youtu.be/nY4XQDsZzFY)


# Indentation and Comments

## IF-ELSE
```python
if True:
    print("Inside if block")
else:
    print("Inside Else block")
```

[![Python IF-ELSE](https://img.youtube.com/vi/lE3IGtyXjLg/0.jpg)](https://youtu.be/lE3IGtyXjLg)


```python
a=10
b=20
if a>b:
    print("a is greater than b")
else:
    print("a is not greater than b")
```


## IF-ELIF
```python
x = 10
if x > 10:
    print("x is greater than 10")
elif x == 10:
    print("x is exactly 10")
elif x < 10:
    print("x is less than 10")
```

## IF-ELIF-ELSE
```python
x = 10
if x > 10:
    print("x is greater than 10")
elif x == 10:
    print("x is exactly 10")
else:
    print("x is less than 10")
```
A more general format would be
```python
if condition:
    pass
elif condition:
    pass
else:
    pass
```

[![Python IF-ELIF-ELSE](https://img.youtube.com/vi/YDBZ0rban3M/0.jpg)](https://youtu.be/YDBZ0rban3M)


## Nested IFs
You can also nest conditional statements for more complex checks
```python
x = 15
if x > 10:
    print("x is greater than 10")
    if x > 20:
        print("x is also greater than 20")
    else:
        print("x is not greater than 20")
```

# Indexing and Slicing Operation

## Python Split and Join

[![Python split join](https://img.youtube.com/vi/_W--TwDA6Nk/0.jpg)](https://www.youtube.com/watch?v=_W--TwDA6Nk)

# Loops & Functions in Python
## For Loop
For loops can be applied on any sequential object (list, string, tuple, range, etc.)
```python
for char in "Hello":
    print(char)
```

```python
for i in range(10):
    print(i)
```

[![Python For Loop](https://img.youtube.com/vi/oywGQ0wVJQs/0.jpg)](https://youtu.be/oywGQ0wVJQs)


## While Loop
```python
i = 1
while i<=10:
  print(i)
  i = i+1
```

[![Python For While Loop](https://img.youtube.com/vi/6mKpZdIfnew/0.jpg)](https://youtu.be/6mKpZdIfnew)


### Continue
### Break
[![Python Continue-break](https://img.youtube.com/vi/Vv8YQqvg4KQ/0.jpg)](https://youtu.be/Vv8YQqvg4KQ)

### Pass Keyword

# Functions in Python
[![Python Intro to Functions](https://img.youtube.com/vi/a3tlV9LZ6aQ/0.jpg)](https://youtu.be/v=a3tlV9LZ6aQ)

## Built-in Functoins

## Custom Functions
```python
def greet():
  return "Good morning"
greet()
```


### Function arguments

[![Python Continue-break](https://img.youtube.com/vi/DHfuVRoTC9o/0.jpg)](https://youtu.be/v=DHfuVRoTC9o)

```python
def add(a,b):
  c = a+b
  return c
z = add(2,4)
print(z)
```

### Default arguments
```python
def add(a,b=10):
  c = a+b
  return c

z = add(2)
print(z)
```
[![Python Default Arguments](https://img.youtube.com/vi/96JrQ1cZsSQ/0.jpg)](https://youtu.be/v=96JrQ1cZsSQ)


### kwargs

### Function return values

```python
def simple_arithmetic(a,b):
  return a+b, a-b, a*b, a/b

tsum, tdiff, tmul, tdiv = simple_arithmetic(10,5)
print(tsum, tdiff, tmul, tdiv)
```

# Basic Library Usage
## Keyword library

[![Python Library](https://img.youtube.com/vi/TA3n-txytck/0.jpg)](https://youtu.be/TA3n-txytck)

## Key Data Science and Machine Learning Libraries
[![DSML Library](https://img.youtube.com/vi/gABxNYVrLKg/0.jpg)](https://youtu.be/gABxNYVrLKg)

# Creating and Using Custom Modules

# File Handling
## OS Library usage