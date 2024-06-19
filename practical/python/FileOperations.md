## Working with txt files : 
__1) working with files in python__
```
with open('sample.txt','r') as file :
    content=file.read()
    print(content)
```
__2) Reading the file content line by line__
```
with open('sample.txt','r') as file:
    for line in file:
        print(line.strip())
```
__3) Overwrite a file content__
```
with open('sample.txt','w') as file:
    file.write("This will overwrite the earlier content.\n")
    file.write("earlier content was of 4 lines\n")
```
__4) Appending the file content using open method__
```
with open('sample.txt','a') as file:
    file.write("This will append the line to the file instead of overwriting\n")
```
__5) Writing a list of lines to a file__
```
strlist = ["Hello\n","World\n","This is another line from list\n"]

with open('sample.txt', 'a') as file :
    file.writelines(strlist)
```
__6) Copying a txt from source file to destination file__
```
with open('sample.txt','r') as file:
    content = file.read()

with open('destination.txt','w') as file:
    file.write(content)

```

## Working with binary files 
__1) Writing a binary file__
```
data = b'\x00\x01\x02\x03\x04'
with open('sample.bin','wb') as file:
    file.write(data)
```
__2) Reading a binary file__
```
with open('sample.bin','rb') as file:
    content = file.read()
    print(content)
```
