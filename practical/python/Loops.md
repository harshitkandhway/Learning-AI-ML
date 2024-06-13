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
