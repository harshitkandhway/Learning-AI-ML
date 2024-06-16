## Dictionary Topics :
1) Introduction to dictionaries
2) Creating dictionaries
3) Accessing dictionary elements
4) Modifying dictionary elements
5) Dictionary methods
6) Iterating over dictionaries
7) nested dictionaries
8) Dictionary comprehension
9) Practical example using dictionaries

## 1) Introduction to dictionary
* Dictionary are unordered collection of items.
* They store data in key-value pair
* Keys must be unique and immutable(strings, numbers, tuples)
* values can be of any type

## 2) Creating Dictionary
* Creating an empty dictionary
```
var = {}
type(var)

Output :
dict
```
* Using dict()
```
student = {'name' : "Alice",'age':20,'country':"USA"}
print(type(student))
dict_example = dict()
print(type(dict_example))

Output :
<class 'dict'>
<class 'dict'>
```
## 3) Accessing dictionary elements
```
dic = {'name' : "Alice",'age':20,'country':"USA"}
print(dic)
print(dic["age"])
print(dic.get("name"))

```
## 4) Nested dictionary
```
nested_dict = {'key1':{'name' : "Alice",'age':20,'country':"USA"},'key2':{'name' : "Bob",'age':26,'country':"UK"}}
nested_dict['key1']['name']
```
## 5) Dictionary methods
* keys()
* values()
* items()
```
for nested_key in nested_dict.keys():
    individual_dict = nested_dict.get(nested_key)
    for individual_key in individual_dict.keys():
        print((individual_key,individual_dict.get(individual_key)))
    print()

Output:
('name', 'Alice')
('age', 20)
('country', 'USA')

('name', 'Bob')
('age', 26)
('country', 'UK')
```
Example 2.
```
for key,value in nested_dict.items():
    print(f"{key}:{value}")
    for key1,value1 in value.items():
        print(f"{key1}:{value1}")

Output :

key1:{'name': 'Alice', 'age': 20, 'country': 'USA'}
name:Alice
age:20
country:USA
key2:{'name': 'Bob', 'age': 26, 'country': 'UK'}
name:Bob
age:26
country:UK
```
## 6) Dictionary Comprehension 
```
same = {x:x*x for x in range(5)}
print(same)

Output :
{0: 0, 1: 1, 2: 4, 3: 9, 4: 16}
```
### Dictionary comprehension with a conditional statement
### Print square of first 10 numbers in a dictionary with a condition number should be even
```
{x:x**2 for x in range(10) if(x%2==0)}

Output :
{0: 0, 2: 4, 4: 16, 6: 36, 8: 64, 10: 100} 
```
## 7) practical examples
* Use a dictionary to count the frequency of elements in a list
```
## Implementation 1)
numbers = [1,2,2,3,3,3,4,4,4,4,5,5,5]
frequency={}
for number in numbers:
    if(number in frequency):
        frequency[number]+=1
    else:
        frequency[number]=1
print(frequency)


## Implementation 2)
numbers = [1,1,1,1,2,2,3,3,3,4,4,4,4,1,5,5,5]
result = {x:numbers.count(x) for x in numbers}
print(result)

Output:
{1: 5, 2: 2, 3: 3, 4: 4, 5: 3}
```

## 8) Concept of Shallow Copy in dictionary

ow to use copy() in dictionary method?
When we use the copy() method, Python creates a completely new dictionary object to store a copy of the reference values from the original dictionary. 
However, the = operator only creates a new reference that remains linked to the original dictionary.
```
## After using copy()

a = {'name' : "Alice",'age':20,'country':"USA"}
b = a.copy()
a['name']="Bob"
print(a)
print(b)

Output:
{'name': 'Bob', 'age': 20, 'country': 'USA'}
{'name': 'Alice', 'age': 20, 'country': 'USA'}
```
```
## If we are not using the copy() instead using assignment operator
a = {'name' : "Alice",'age':20,'country':"USA"}
b = a
a['name']="Bob"
b['country']="India"
print(a)
print(b)

Output:
{'name': 'Bob', 'age': 20, 'country': 'India'}
{'name': 'Bob', 'age': 20, 'country': 'India'}
```
