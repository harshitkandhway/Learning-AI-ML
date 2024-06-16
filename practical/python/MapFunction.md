## Map Function 
The map() function executes a specified function for each item in an iterable. The item is sent to the function as a parameter

Example:
If we have to apply a function on a collection of item like list, tuple or dictionary, we can use map function like below:

1) Squaring all the numbers in the list
```
numbers=[2,3,4,5]
result = list(map(lambda x:x*2,numbers))
print(result)

Output :
[4,6,8,10]
```

2) Printing all the names of student from the dictionary
```
student = [{'name' : "Alice",'age':20,'country':"USA"},{'name':"Bob",'age':22,'country':"UK"},{'name':"Chetan",'age':28,'country':"India"}]
get_name = lambda x:x.get('name')
names = list(map(get_name,student))
print(names)

Output :
['Alice', 'Bob', 'Chetan']
```
3) Write a code to print square of the numbers of the above list.
```
objs = [2,3,5,4,1]
## Using List comprehension 
result = [x**2 for x in objs]
print(result)

## Implementation using normal programming
for x in objs:
    print(f"{x**2} ")

## Using lambda and map function
res = map(lambda x:x**2 ,objs)
print(list(res))

Output :
[4, 9, 25, 16, 1]

4 
9 
25 
16 
1
 
[4, 9, 25, 16, 1]

```
