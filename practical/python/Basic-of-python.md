## single line command
```
"""
This is multiline comment 
Hi line 2
"""
```

## Multiple statments getting executed in single line
```
i=12;j=4;z=i+j
print(z)
```

## This is line continuation in python using backslash
```
d=2+4+7+1+1+1\
    +5
print(d)
```
## Name Error happens at b=c since c is not defined :
ex:) print(u)
```
---------------------------------------------------------------------------
NameError                                 Traceback (most recent call last)
Cell In[53], line 1
----> 1 print(u)

NameError: name 'u' is not defined
```

## Type Inference happens by default in python during runtime, hence we dont have to declare the type of variable being used.
```
a=2
b=type(a)
c="abc"
print(type(a))
print(type(b))
print(type(c))
```
## Indentation plays a vital role in python
```
a=4
    f=9
print(a)

We will get IndentationError as below: 
Cell In[14], line 28
    f=9
    ^
IndentationError: unexpected indent
```

## Python is case sensitive
```
name = "Hello"
Name = "World"
print(name)
print(Name)
```

