##  Loops in python can be implemented using for loop and while loop

### For loop example : 
```
for i in range(0,10,1):
    print(i)
```
In the above example : 
* first argument is the starting index of the range, if not given it will default to 0.
* second argument is the upper limit of the range but it in never included in the loop for example the loop runs at second_argument-1 in the last loop if step is declared as 1.
* third argument in the range method defines the step.

### Nested loop example using for loop

If we have to print a pattern like :
```
#
##
###
####
#####
```
```
text=""
for i in range(6):
    for j in range(i):
        text+="#"
    text+="\n"
print(text)

```
### While loop example
For printing the numbers from 5 to 1 using while loop :
```
i=5
while i>0:
    print(i)
    i-=1
```

## Working with break, continue and pass in the loops

## Continue will just skip the specific looping condition
Code below will only print odd numbers from 1 to 9 :
```
for i in range(10):
    if(i%2==0):
        continue
    print(i)
```

## break will break the loop execution at the specific conditional statement
Code below will only print 1,2 and 3 and then break from execution :
```
i=0
while(i<5):
    print(i)
    if(i==3):
        break
    i+=1
```

## pass does nothing while working in the loops
Code below prints all the numbers from 1 to 9 :
```
for i in range(0,10):
    if(i%2==0):
        pass
    print(i)
```
