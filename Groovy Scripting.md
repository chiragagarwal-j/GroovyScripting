# Groovy Basics

Groovy is case-sensitive

## Comments in Groovy

1. Single-line comment: `//`

2. Multi-line comments:

   ```groovy
   /*
   ----
   ----
   ----
   ----
   */

## Documentation 
- purpose of the script 
- Display Hello world statement
- date 
- version
- Author name

## Groovy one liner 
```
groovy -e "println 'Hello world'"
```

## Variable
- It is used to store the data. The data can be any data type(int/float/bool/string)
- Groovy uses dynamic data type 

## Types of variables in groovy
1) scalar 
2) Arrays or List 
3) Hash Map or Dictionary

## Get data type
It is used to display the data type of the variable
```
a = 10
b = 2.5
c = "groovy"
d = 'G'

println d.getClass()
```
## Interpolation
Getting variable substitution between a double quotes
```
println "The variable a value is : " + a
print "The variable a value is : $a"
```
## scalar 
It holds only one single value. The data can be any data type 

- int 
- float
- bool
- strings

## strings 
1) single quoted string ' '
2) double quoted strings " "

Quoting rules 
===============
```' ' '``` Not accepted

```" " "``` Not accepted

```' " '``` accepted

```" ' "``` accepted

```' \' '``` accepted

```" \" "``` accepted

Example:
```
println "Hi , \"from Groovy"
println 'Hi , \' from Groovy'
println "Hi, Groovy's script"
println 'Hi, this is Groovy"s script'
```
### Types of Case
1. Camel Case
```studentName='Siri'```

2. Snake Case 
```student_name='Siri'```

3. Pascal case 
```StudentName='siri'```

## Function vs Methods 

### Function or sub routines or procedures
- Function we can define outside of the class. 
- Function we can call directly with function name.

**eg : functionname()**

### Methods
- Methods we can create inside of the class.
- Methods we can call with object statement.

**eg : variablename.methodname()**

## String built in methods
 1) length()
 2) substring()
 3) indexof()
 4) replace()
 5) toLowerCase()
 6) toUpperCase()
 7) reverse()
 8) split()
 9) join()
---
1) length()

  It is used to get the length of the given string 
	
2) substring()

  It is part of the string

3) indexOf()

  It is used to get the specific character index num
 
4) replace()

   It is used to replace the character with new character
 
5) toLowerCase()

 Converting to lowecase 
 
6) toUpperCase()

  Converting into uppercase

7) reverse()

  Display reverse order of the string 

 8) split()

  It is used to split single string to multiple string based on delimiter.
 
  space is a default delimiter

eg: **, . : ; tabsapce** 
 
9) join()
    
It is used to join multiple strings to single string

Example for String in-built in methods:

```
str = "Groovy scripting"
println "length of str: "+str.length()
println "substring: "+str.substring(0,5)
println "index Of G is:"+str.indexOf('G')
println "replace o with i: "+str.replace('o','i')
println "toLowerCase: "+str.toLowerCase()
println "toUpperCase: "+str.toUpperCase()
println "reverse: "+str.reverse()
println "split by space: "+str.split()
println "join multiple strings: "+str.split().join(" 2.0 ")
```
Example for split method and join method
```
user_info = "siri:x:10001:10001:Hyd:/home/siri:/bin/shell"
println user_info.split(':')[0]

file_info = "22Dec2023 192.161.1.10 80 192.161.1.11 88 web.cgi"
println file_info.split()[1..4].join(" ")
```
## Taking input from user/keyboard
```
name = System.console().readLine "Enter your name:"
println "Hello $name from Groovy"
```

## Typecasting
```
num1 = System.console().readLine "Enter num1 : "
num2 = System.console().readLine "Enter num2 : "
num1 = num1 as int
sum = num1 + num2.toInteger()
println "Sum of $num1 and $num2 is $sum"
```

## Operators
1. Arithmatic Operators: +, -, *, /, %
2. Relational Operators: >, <, >=, <=, ==, !=
3. Logical Operators: &&, ||, !
4. Assignment Operator: =
5. Short Hand Assignment Operators: +=, -=, *=, /=
6. Inc/Dec Operators: i++, ++i, --i, i--
7. String concatination: +
8. String Repetition Operator: *

Example for String Repetition:
```
x = "groovy "
println x * 4
```
## Conditional statements
1) simple if 
2) if else 
3) ladder if (if else if )
4) nested if 
5) switch case

```
num1 = System.console().readLine "Enter any num to check even or odd: "
if (num1.toInteger() %2 == 0){
	println "$num1 is a even number"
}
else if (num1.toInteger() %2 != 0) {
	println "$num1 is a odd number"
}
else {
	println "Entered number is not integer"
}
```

```
num1 = System.console().readLine "Enter any num to check num is 3 digit or not: "
if (num1.toInteger() >99 && num1.toInteger() <1000){
	println "$num1 is a 3 digit number"
}
else {
	println "Entered number is not a 3 digit number"
}
```

```
num1 = System.console().readLine "Enter any num : "
num1 = num1.toInteger()
if(num1>0)
	println "Positive Number"
else if (num1<0)
	println "Negative Number"
else if (num1 == 0)
	println "Entered num is 0"
```

```
println"\n\n\n\n\t\t\t\tFood Menu\n\t\t\t\t**** ****\n1.Veg Menu\n2.Non Veg Menu\n3.Jain Menu\n\n"
option = System.console().readLine "Enter your menu option: "
option = option.toInteger()
if(option == 1){
	println"1.Panner\n2.Butter Naan"
}
else if(option == 2){
	println"1.Chicken"
}
else{
	println"1.Jain Curry"
}
```

```
a = System.console().readLine "Enter num1: "
b = System.console().readLine "Enter num2: "
println"\n\n\n\n\t\t\t\tArithematic Operations\n\t\t\t\t*********** **********\n1.Sum\n2.Sub\n3.Mul\n4.Div\n5.Mod\n6.Exponent"
option = System.console().readLine "Enter operation to be performed: "
a = a.toInteger()
b = b.toInteger()
option = option.toInteger()
if(option ==1){
	println"${a+b}"
}
else if (option == 2){
	println"${a - b}"
}
else if (option == 3){
	println"${a * b}"
}
else if (option == 4){
	println"${a / b}"
}
else if (option == 5){
	println"${a % b}"
}
else if (option == 6){
	println"${a ** b}"
}
```

```
a = System.console().readLine "Enter num1: "
a = a as int
if(a > 0){
	println "$a is positive"
	if(a < 10){
		println "$a is a single digit number"
		if(a % 2 == 0){
			println "$a is single digit even number"
		}
		else if(a % 2 != 0){
			println "$a is single digit odd number"
		}
	}
	else{
		println "$a is not a single digit"
	}

}
else if(a < 0){
	println"$a is negative"
}
else if(a == 0){
	println "$a is zero"
}
```
```
num=System.console().readLine "Enter a number:"
num = num as int
switch(num){
	case 1:
		println "Entered number is 1"
		break
	case 2:
		println "Entered number is 2"
		break
	case 3:
		println "Entered number is 3"
		break
	case 4:
		println "Entered number is 4"
		break
	default:
		println "Invalid number"
}
```

**switch statements using range operator**

```
num=System.console().readLine "Enter a number:"
num = num as int
switch(num){
	case 1..10:
		println "Entered number is $num"
		break
	
	default:
		println "Invalid number"
}
```

## Loops 
1) while
2) for 
3) for in

Program to enter ATM pin, 3 entries only
```
i = 1

while(true){
	if(i>3){
		println "To many incorrect tries, your account has been blocked"
		break
	}
	num=System.console().readLine "Enter your ATM pin:"
	num=num as int
	if(num==1234){
		println "Successfully Logged In"
		break
	}
	else{
		println "Incorrect Pin, try again"
	}
	i++
}
```

for loop
```
for (i in 1..10){
	println i
}
```
```
for(i=1;i<10;i++){
	println i
}
```
```
list = [10,20,30,40]
for (i in list){
	println i
}
```

## Loop control statements
1) continue
2) break

Display 1 to 10 except 5
```
for(i = 1; i < 11; i++){
	if(i == 5){
		continue
	}
	println i
}
```

script to display 1 to 50 such that 
print fizz for multiples of 3,
print buzz for multiples of 5,
print fizzbuzz for multiples of 3 & 5
```
for (i in 1..50){
	if( i % 3 == 0 && i %5 == 0){
		println "FizzBuzz"
	}
	else if (i % 3 == 0) {
		println "Fizz"
	}
	else if(i % 5 == 0) {
		println "Buzz"
	}
	else {
		println i
	}
}
```

## switch statements using regex
- **+** It matches 1 or more occurences of preceding character
- **[]** It matches any one character from the given list or range
- **^** It matches any one character other than the given list or range
- **~** It is true, if pattern matches

Script to display given input is any characters of follows:
is a alphabet, is a digit, is special char

```
ch = System.console().readLine "Enter any character : "
switch(ch){
	case ~/[a-zA-z]/:
		println "It is a alphabet"
		break
	case ~/[0-9]/:
		println "It is a digit"
		break
	case ~/[^0-9a-zA-z]/:
		println "It is a special character"
		break
	default:
		println "Not Matched"
}
```

## Arrays or List or Indexed Array
- Collection of similar data type is an Array in programming lang.
- Collection of any data items is array in groovy.

eg:
```
list = [10,20,"Groovy"]

println list

for (i in list){
	println i
}

println list[0,2]

println list[0..2]

list [2] = "linux"
println list
```

- We can access values based on index or reverse index. 
- Index start with 0 and reverse index start with -1.

## Array methods

 1) size() : It is used to get the total size of the array.
 2) count()  : It  is used to display number of occurences of the given value.
 3) remove()  : It is used to delete a value based on index number.
 4) pop() : It is used to delete a last value from the array
 5) sort() : It is used to display all the values in ascending order
 6) reverse() : It is used to display all the values in reverse order
 7) add()  : It is used to add a new value at end of the array
 8) contains() : It is used verify the given value exist or not
 9) push() : It is used all new value at before 0th index
 10) drop() : It is used to drop the values from the list.

Example:

```
ls = [10, 20, "Groovy", 5.5, 7.62]

println ls

println "size: " + ls.size()

println "count of 10: " + ls.count(10)

ls.remove("Groovy")
println "remove 'Groovy': " + ls

ls.pop()
println "pop: " + ls

println "sorting: " + ls.sort()

println "reversing: " + ls.reverse()

ls.add(15)
println "Adding 15: " + ls

println "check 3 is in list: " + ls.contains(3)

ls.push(0)
println "push 0 to list: " + ls

println "drop first 2 values: " + ls.drop(2)
```
