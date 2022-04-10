## Operators

Operators are symbols or pairs of symbols which represent special functions on one or more values. In Stensl, most operators are infix, meaning that their arguments are placed to either side, though operators may also be prefix, meaning that a singular argument is placed following the operator. There is also one operator, the element grab operator, which has special rules as to how its arguments are placed, these are explained in the element grab subsection. In some cases, operators may share a symbol, in which case the interpreter disambiguates based on argument type. For instance, in the expression `2+2`, int addition is used, whereas in the expression `2+2.0`, float addition is used because it is the only operator compatible with both arguments’ types. A complete list of operators is available below:


### Addition

Position: infix

Symbol: +

Left type: float

Right type: float

Result type: float

Precedence: Additive

Description: Adds two floating points.


### Multiplication

Position: infix

Symbol: *

Left type: float

Right type: float

Result type: float

Precedence: Multiplicative

Description: Multiplies two floating points.


### Subtraction

Position: infix

Symbol: -

Left type: float

Right type: float

Result type: float

Precedence: Additive

Description: Subtracts two floating points.


### Division

Position: infix

Symbol: /

Left type: float

Right type: float

Result type: float

Precedence: Multiplicative

Description: Divides two floating points. Throws an error if the right argument is zero.


### Modulo

Position: infix

Symbol: %

Left type: float

Right type: float

Result type: float

Precedence: Multiplicative

Description: Returns the remainder of the division of two integers. Throws an error if the right argument is zero


### Int Addition

Position: infix

Symbol: +

Left type: int

Right type: int

Result type: int

Precedence: Additive

Description: Adds two integers.


### Int Multiplication

Position: infix

Symbol: *

Left type: int

Right type: int

Result type: int

Precedence: Multiplicative

Description: Multiplies two integers.


### Int Subtraction

Position: infix

Symbol: -

Left type: int

Right type: int

Result type: int

Precedence: Additive

Description: Subtracts two integers.


### Int Division

Position: infix

Symbol: /

Left type: int

Right type: int

Result type: int

Precedence: Multiplicative

Description: Divides two integers and returns the truncated result. Throws an error if the right argument is zero.


### Int Modulo

Position: infix

Symbol: %

Left type: int

Right type: int

Result type: int

Precedence: Multiplicative

Description: Finds the remainder of the division of two integers.


### Concatenation

Position: infix

Symbol: &

Left type: string

Right type: string

Result type: string

Precedence: Additive

Description: Returns the concatenation of two strings.


### Character Grab

Position: infix

Symbol: $

Left type: string

Right type: int

Result type: char

Precedence: Multiplicative

Description: Returns the character that lies at a particular index within its left argument, where the index is defined by the right argument. The index zero represents the first character of the string.


### Float Equality

Position: infix

Symbol: ==

Left type: float

Right type: float

Result type: bool

Precedence: Comparative

Description: Returns whether two floating points are equal.


### String Equality

Position: infix

Symbol: ==

Left type: string

Right type: string

Result type: bool

Precedence: Comparative

Description: Returns whether two strings are equal.


### Bool Equality

Position: infix

Symbol: ==

Left type: bool

Right type: bool

Result type: bool

Precedence: Comparative

Description: Returns whether two boolean values are equal.


### Float Inequality

Position: infix

Symbol: !=

Left type: float

Right type: float

Result type: bool

Precedence: Comparative

Description: Returns whether two floating points are unequal.


### String Inequality

Position: infix

Symbol: ==

Left type: string

Right type: string

Result type: bool

Precedence: Comparative

Description: Returns whether two strings are unequal.


### Bool Inequality

Position: infix

Symbol: ==

Left type: bool

Right type: bool

Result type: bool

Precedence: Comparative

Description: Returns whether two boolean values are unequal.


### Less Than

Position: infix

Symbol: &lt;

Left type: float

Right type: float

Result type: bool

Precedence: Comparative

Description: Returns whether the left argument is less than the right argument.


### Greater Than

Position: infix

Symbol: >

Left type: float

Right type: float

Result type: bool

Precedence: Comparative

Description: Returns whether the left argument is greater than the right argument.


### Less Than or Equal to

Position: infix

Symbol: &lt;=

Left type: float

Right type: float

Result type: bool

Precedence: Comparative

Description: Returns whether the left argument is less than or equal to the right argument.


### Greater Than or Equal to

Position: infix

Symbol: >=

Left type: float

Right type: float

Result type: bool

Precedence: Comparative

Description: Returns whether the left argument is greater than or equal to the right argument.


### Divisibility

Position: infix

Symbol: %%

Left type: float

Right type: float

Result type: bool

Precedence: Comparative

Description: Returns whether the left argument is divisible by the right argument. Throws an error if the right argument is zero.


### Conjunction

Position: infix

Symbol: &&

Left type: bool

Right type: bool

Result type: bool

Precedence: Conjunctive

Description: Returns whether both the left and right arguments are true.


### Disjunction

Position: infix

Symbol: ||

Left type: bool

Right type: bool

Result type: bool

Precedence: Disjunctive

Description: Returns whether either the left and right arguments are true.


### Negation

Position: prefix

Symbol: !

Argument type: bool

Result type: bool

Precedence: Negative

Description: Returns the logical negation of the argument


### Function Piping

Position: infix

Symbol: |

Left type: (any)->any

Right type: the argument type of the left argument

Result type: the result type of the left argument

Precedence: Functional

Description: Returns the result of the left function when the right argument is applied to it.


### Element Grab

Position: infix/postfix

Symbol: []

Left type: [any]

Right type: int

Result type: The type of an element of the left argument

Precedence: Functional

Description: This returns an element at a particular index of an array. The array goes to the left of the operator and is considered its left argument. The index from which to get the element goes between the “[” and “]” symbols and is considered its right argument. Arrays in Stensl index at zero, thus the index zero references the first element of the array.

Examples of proper usage of the element grab operator are below:


```
someArray[5]
someArray[2213]
someArray[0] //references the first element of the array
```
