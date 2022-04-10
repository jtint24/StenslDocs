## Built-in Functions

Stensl has a wide array of built-in functions that are used alongside operators to construct expressions. While they are similar to operators in that they produce a result from one or more arguments, they are still distinct. Built-in functions tend to have smaller sets of use cases and functionality that could not be described with a single symbol without being cryptic. This necessitates their being functions rather than operators. For more information on functions in  general, turn to the section on functions. Built-in functions cannot be used in a first class context because they are implemented on a level below Stensl for performance and consistency purposes.

Below is a complete list of built-in functions in Stensl:


### str

Type: `(any)->string`

Description: Converts a value of another type to a string

Usage examples:


```
str(4) // result: "4"
str(true) // result: "true"
```



### int

Type: `(any)->int`

Description: Converts a value of another type to an integer

Usage examples:


```
int("4") // result: 4
int(3.0) // result: 3
```


 


### float

Type: `(any)->float`

Description: Converts a value of another type to a float

Usage examples:


```
float("4") // result: 4.0
float(3) // result: 3.0
```



### print

Type: `(any)->void`

Description: Prints a value to the console

Usage examples:


```
print("hello there") // result: prints "hello world"
print(true) // result: prints "true"
```



### println

Type: `(any)->void`

Description: Prints a value to the console and follows it with a newline character

Usage examples:


```
print("hello there") // result: prints "hello world" and jumps to a new line
print(true) // result: prints "true" and jumps to a new line
```



### assert

Type: `(bool)->void`

Description: Evaluates a boolean value and throws an error if the value is false

Usage examples:


```
assert(4==4) // does nothing
assert(4==3) // throws an error
```



### ascii

Type: `(int)->char`

Description: Gets an index from the user and returns the character that lies at that position on the ascii table.

Usage examples:


```
ascii(34) // result: " 
ascii(65) // result: A
```



### typeof

Type: `(any)->string`

Description: Gets the name of the type of a value as a string

Usage examples:


```
typeof(ascii(4)) // result: "char"
typeof([1, 2, 3]) // result: "[int]"
```



### input

Type: `(string)->string`

Description: Inputs a string and prints it to the console then skips to a new line, unless the string is blank, in which case it does not print anything. It then accepts a line of input from the user and returns their input as a string.

Usage examples:


```
input("") // accepts a line of input
input("What is your name?") // prints out "What is your name?" then accepts a line of input on a new line.
```



### throw

Type: `(string)->void`

Description: Inputs a string and then throws an error with the first argument as the error message.

Usage examples:


```
throw("This section should be unreachable!")
```