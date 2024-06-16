## Filter Function
Python's filter function uses an iterable to test each element's truth value. This allows the function to filter a specified sequence.

Example : 
1) filter all the numbers which are greater than 5 in the list using lambda and filter method
```
numbers = [3,5,8,1,89,34,56,0,2,6,99,8,0,7,9,5,7,23,1,4,5,7,8]

fun_lt = lambda x:x<5
result = list(filter(fun_lt,numbers))
print(result)
```
Output: 
```
[3, 1, 0, 2, 0, 1, 4]
```

2) filter the students from the dictionary where the age of the student is greater than 25.

```
student = [{'name' : "Alice",'age':29,'country':"USA"},{'name':"Bob",'age':22,'country':"UK"},{'name':"Chetan",'age':28,'country':"India"}]

def age_gt_25(people):
    return people['age']>25

result = list(filter(age_gt_25,student))
print(result)
```
Output : 
```
[{'name': 'Alice', 'age': 29, 'country': 'USA'}, {'name': 'Chetan', 'age': 28, 'country': 'India'}]
```
