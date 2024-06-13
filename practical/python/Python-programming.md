## Write a program to check if a year is a leap year
year = int(input("Enter the year"))
if year%4==0:
    if year%100==0:
        if year%400==0:
            print("Year : "+str(year)+ " is a leap year")
        else:
            print("Year "+str(year)+" is not a leap year")
    else:
        print("Year "+str(year)+" is a leap year")
else:
    print("Year "+str(year)+" is not a leap year")


## Write a program to denote a simple calculator with operators as input from user
first = float(input("Enter first number"))
second = float(input("Enter secont number"))
operator = input("Enter the operation which you want to perform(+,-,*,'\',%)")
if operator=='+':
    result=first+second
elif operator=='-':
    result=first-second
elif operator=='*':
    result=first*second
elif operator=="/":
    if second==0:
        result="Divide by zero exception : Number cannot be divided by zero"
    else:
        result=first/second
elif operator=="%":
    result==first%second
else:
    result="Invalid operator selected"
print(result)
