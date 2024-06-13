## 1) Working with list in python :
* Creating list
```
## directly assign it to the value
words = ["first","second"]

## use list() function
numbers = list((1,2,3,4,5))
```

* Accessing list items
```
## This prints the word at the 0 index
print(words[0])

## This prints last element of the list
print(numbers[-1])
```

* Updating an element at specific index
```
## using index directly
numbers[0]=4

## using append() to add at the last index
numbers.append(12)

## remove the number at last index and return the number
popped_num = numbers.pop()
print(popped_num)

## remove element of the list
numbers.remove(3)

## what happens if you try to remova a number from list which is not present
numbers = [1,2,30,4,5,12]
print(numbers)
numbers.remove(3)
print(numbers)

Output of the code : 
---------------------------------------------------------------------------
ValueError                                Traceback (most recent call last)
Cell In[92], line 3
      1 numbers = [1,2,30,4,5,12]
      2 print(numbers)
----> 3 numbers.remove(3)
      4 print(numbers)

ValueError: list.remove(x): x not in list
```

* Slicing operations in list
```
numbers=[1,2,3,4,5,6,7,8,9,10]
print(numbers[:2])
print(numbers[5:])
print(numbers[2:5])
print(numbers[::2])
print(numbers[::-1])

Output of the above staments : 

[1, 2]
[6, 7, 8, 9, 10]
[3, 4, 5]
[1, 3, 5, 7, 9]
[10, 9, 8, 7, 6, 5, 4, 3, 2, 1]

```
## 2) Working with enumerate method for finding and printing index and value 
```
numbers=[1,2,3,4,5,6,7,8,9,10]
for ind,number in enumerate(numbers):
    print(ind, number)
```
Output for the above example :
```
0 1
1 2
2 3
3 4
4 5
5 6
6 7
7 8
8 9
9 10
```
## 3) Create a list which contains square of first 10 numbers
```
tmp=[]
for i in range(10):
    tmp.append(i**2)
print(tmp)
```
Output for the above code :
```
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```
## 4) List Comprehension
* Basic Syntax[expression for item in iterable]
  Printing a list containing square of first 10 numbers using list comprehension :
  ```
  print([x*x for x in range(10)])
  ```
* Syntax with conditional logic[expression for item in iterable if condition]
  Printing a list containing square of first 10 numbers only if the numbers are even
  ```
  print([x*x for x in range(1,11) if(x%2==0)])
  ```
  Output
  ```
  [4, 16, 36, 64, 100]
  ```
## 5) Nested List Comprehension
```
first=[1,2,3]
second=['a','b']
res = [[i,j] for i in first for j in second]
print(res)
```
Output for the above code :
```
[[1, 'a'], [1, 'b'], [2, 'a'], [2, 'b'], [3, 'a'], [3, 'b']]
```
## 6) List Comprehension with function calls

Write a code which prints length of each word present in a list of words.
```
words = ["apple","banana","kiwi","watermelon"]
print([len(word) for word in words])
```
Output for the above code:
```
[5, 6, 4, 10]
```
