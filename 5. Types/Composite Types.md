## Composite Types

A composite type is one which is constructed from one or more other types, but is not compatible with another type. In Stensl, there are two ways to form a composite type: with functions and with arrays.


### Function Types

Because functions are first-class citizens in Stensl, they must have types. Function types are created from the types of all of their arguments in order, as well as the type of their return value. Note that void functions return void. To represent these types in code, their argument types are put into a parenthesized comma-separated list, followed by a “->” and the return type of the function. Note that no spaces are allowed in the names of function types (or any types) to make the name look like a single identifier. 

For instance, the following are valid function types:



* `(int)->void`
* `(int,string)->char`
* `(int,(string,int)->char)->float`
* `(float,char)->(bool,char)->void`

### Array Types

Array types are the other kind of composite type available in Stensl. An array type is created from the type of the elements of the array. The name of these types is the name of the type of the elements enclosed in square brackets.

For instance, the following are valid array types:



* `[int]`
* `[[string]]`
* `[(int)->[bool]]`

