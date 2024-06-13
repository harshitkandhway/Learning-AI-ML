## Topics to be covered for tuples
1) Introduction to tuples
2) Creating tuples
3) Accessing tuple elements
4) tuple operations
5) Immutable nature of tuples
6) tuple methods
7) Packing and unpacking tuples
8) nested tuples
9) Practical Examples and Common Errors

### Introduction to Tuples
Tuples are ordered collection of items that are immutable. These are very similar to Lists but are immutable unlike Lists.

### Creating tuples
We can create tuples in many ways : 
* creating empty tuple
```
empty_tuple = ()
print(type(empty_tuple))

Output :
<class 'tuple'>
```
* using tuple()
```
numbers = tuple([1,2,3,4,5,6,7])
numbers

Output:
(1, 2, 3, 4, 5, 6, 7)
```
* Directly assigning values to tuple
```
words = ("first","second","third","fourth","fifth")
print(words)
type(words)

Output:
('first', 'second', 'third', 'fourth', 'fifth')
tuple
```
* mixed_tuple example
```
mixed_tuple = (1,"hello",3.14)
mixed_tuple

Output :
(1, 'hello', 3.14)
```
### Accesing Tuples and the slicing operations
```
## accessing elements from tuple
mixed_tuple = (1,"hello",3.14)
print(mixed_tuple[1])
print(mixed_tuple[-1])
print(mixed_tuple[:])
print(numbers[::2])
print(numbers[::-1])
print(numbers[::-2])
print(numbers[2:4])
print(numbers[2:6])

Output :
hello
3.14
(1, 'hello', 3.14)
(1, 3, 5, 7)
(7, 6, 5, 4, 3, 2, 1)
(7, 5, 3, 1)
(3, 4)
(3, 4, 5, 6)
```

### Operations on tuple
```
## Concatenation operation on tuple
concated_tuple=numbers+mixed_tuple
print(concated_tuple)

## Multiplication operation on tuple
multiplied_tuple=mixed_tuple*3
print(multiplied_tuple)
```
### Immutable nature of tuple
Tuples are immutable in nature hence when we try reassinging any index with a value we get error astuple object does not support item assignment
```
numbers[2]=3
---------------------------------------------------------------------------
TypeError                                 Traceback (most recent call last)
Cell In[24], line 1
----> 1 numbers[2]=3

TypeError: 'tuple' object does not support item assignment
```
How to update any element in tuple
We cant since tuples are immutable.
A workaround can be converting tuple into list and then updating the list, and changing back from list to tuple

### Tuple Methods
* numbers.count(2)
* numbers.index(5)

### Packing in a tuple
```
var = 1,"abc",89
print(type(var))
print(var[::-1])

Output :
<class 'tuple'>
(89, 'abc', 1)
```
### Unpacking a tuple
```
a,b,c = var
print(a)
print(b)
print(c)

Output :
1
abc
89
```
### Unpacking a tuple using *
```
var1 = 1,2,3,4,5,6,9.3,"a",True
a,*b,c = var1
print(a)
print(b)
print(c)

Output :
1
[2, 3, 4, 5, 6, 9.3, 'a']
True
```
### Nested Tuple
```
var2 = ((1,2,3),("A","b"),(3.4,True,"abc",7,8,9,0.2))
var2[2][::-1]

Output :
(0.2, 9, 8, 7, 'abc', True, 3.4)
```
### Iterating elements in a nested tuple
```
for sub_tuple in var2:
    for g in sub_tuple:
        print(g,end=" ")
    print()

Output :
1 2 3 
A b 
3.4 True abc 7 8 9 0.2 
```
