Topics to cover : 
1) Introduction to functions
2) Defining functions
3) Calling functions
4) Function Parameter
5) Default parameters
6) Variable length arguments
7) Return statement

## Introduction to Functions
Functions are blocks of code doing a specific task.
Functions helps in code reusability,readability and proper organization of code.

## Defining and Calling Functions
* Basic syntax of a function
```
def my_function_name(para1):
    """Docstring"""
    ## Function body
    print(para1)
```
* Functions with a return statment
```
def my_fun(param1):
  return param1
```
* Function returning multiple values
```
def odd_even(number):
    if(number%2==0):
        return number,0
    else:
        return number,1
```
## Default parameter in fuctions
```
def my_function_name(para1="Default_value"):
    print(para1)

result = my_function_name()
print(result)

Output :
Default_value
```
## Variable length arguments
* postional arguments(*args)
* keyword arguments(**kwargs)
```
## 1) Positional arguments 

def my_fun_pos(*args):
    for arg in args:
        print(f"Positional arguments : {arg}")

## 2) Keyword arguments

def my_fun_kw(**kwargs):
    for key,value in kwargs.items():
        print(f"{key}:{value}")
    
my_fun_pos(1,2,3,4,5)
my_fun_kw(name="Alice",age=20,country="USA")
```
```
Output :
Positional arguments : 1
Positional arguments : 2
Positional arguments : 3
Positional arguments : 4
Positional arguments : 5
name:Alice
age:20
country:USA
```
Note : __Positional argument cannot apear after keyword argument__
If we have a function where both positional arguments and keyword arguments are defined, while calling the function we must mention all the positional arguments sfirst 
then only we should define the keyword arguments, otherwise we will get the error as postional argument cannot appear after keyword argument.
