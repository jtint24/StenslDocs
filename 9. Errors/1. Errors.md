
Errors are events which occur when Stensl code encounters an unresolvable problem which makes continuation of the program impossible. Errors terminate the program and give a description of the event which triggered them. The Stensl error manager will also give the location of the error, as well as a stack trace showing where the line where the error occurred was called from, if any. 

Additionally, all errors are also thrown with error codes. The grammar of an error code is such


```
<error code> ::= <positive integer>.<positive integer>
<positive integer> ::= <digit> | <digit><positive integer>
```


The two numbers which comprise the error code describe where the error occurred within the Stensl interpreter. This can be useful for debugging Stensl code as well as sorting out any irregular behaviors of the interpreter, if they occur. In total, an example Stensl error message looks like this:


```
Error on line 5!
Error details: Division by zero!
Error code: 3.1
Problematic line:	"println(0/0)"
Stack Trace:
	From line number 5
	From line number 7
```


A complete catalog of errors in Stensl is available below. Some error messages contain excerpts from the particular problematic elements of code for clarity; these have been replaced by generalized tokens, denoted inside angle brackets.


<table>
  <tr>
   <td>Message
   </td>
   <td>Cause
   </td>
  </tr>
  <tr>
   <td><code>Cannot mutate a constant!</code>
   </td>
   <td>An attempt has been made to mutate a constant either implicitly or through direct assignment
   </td>
  </tr>
  <tr>
   <td><code>Cannot assign a value of type '&lt;type1>' to a variable of type '&lt;type2>' !</code>
   </td>
   <td>A variable of &lt;type1> has been given a value with the type &lt;type2>, between which conversion is impossible.
   </td>
  </tr>
  <tr>
   <td><code>Cannot increment immutable variable!</code>
   </td>
   <td>An immutable variable has been placed as the index of a for loop and cannot be incremented as it cannot be mutated.
   </td>
  </tr>
  <tr>
   <td><code>Cannot increment non-numerical type, '&lt;type>'</code>
   </td>
   <td>A non-numerical variable of type &lt;type> has been placed as the index of a for loop and cannot be incremented as it is type-incompatible.
   </td>
  </tr>
  <tr>
   <td><code>Cannot get a property from an out-of-scope area!</code>
   </td>
   <td>An attempt has been made to access a property from an area that has been disallowed from accessing the property
   </td>
  </tr>
  <tr>
   <td><code>Cannot call non-existent property '&lt;property>' !</code>
   </td>
   <td>An attempt has been made to access a property, called &lt;property>, from a value of a type which does not have the available property.
   </td>
  </tr>
  <tr>
   <td><code>Array index &lt;index> out of bounds for length &lt;length>!</code>
   </td>
   <td>An array has been indexed with the out-of-bounds number &lt;index>, which is not possible because the array only has &lt;length> elements.
   </td>
  </tr>
  <tr>
   <td><code>Cannot set an array to a non-array!</code>
   </td>
   <td>A non-array has been assigned to an array.
   </td>
  </tr>
  <tr>
   <td><code>Cannot index an array with a non-integer!</code>
   </td>
   <td>An array has been indexed with an expression that does not resolve to an integer.
   </td>
  </tr>
  <tr>
   <td><code>Cannot call non-function '&lt;property>'!</code>
   </td>
   <td>There has been an attempt to call a non-function as a method
   </td>
  </tr>
  <tr>
   <td><code>Cannot set an object to a non-object!</code>
   </td>
   <td>A non-object has been assigned to an object
   </td>
  </tr>
  <tr>
   <td><code>Cannot match given type '&lt;argument type>' to expected type '&lt;operand type>' in argument &lt;argument number> of operation: '&lt;operation name>' !</code>
   </td>
   <td>Within the arguments to an operator or function called &lt;operation name>, a type mismatch has occurred between the expected type &lt;operand type> and the given type &lt;argument type> on the argument number &lt;argument number>
   </td>
  </tr>
  <tr>
   <td><code>Unterminated block comment!</code>
   </td>
   <td>A block comment has been opened but not terminated.
   </td>
  </tr>
  <tr>
   <td><code>Class '&lt;class name>' is not a legal identifier!</code>
   </td>
   <td>The name given to a class, &lt;class name>, is not legal. See the section on legal identifiers to construct a valid one.
   </td>
  </tr>
  <tr>
   <td><code>Unterminated class '&lt;class name>'!</code>
   </td>
   <td>A class body for the class called &lt;class name> has been opened but has never been closed
   </td>
  </tr>
  <tr>
   <td><code>Cannot declare a nested class!</code>
   </td>
   <td>A class has been declared inside of another class
   </td>
  </tr>
  <tr>
   <td><code>Invalid type: '&lt;type>' !</code>
   </td>
   <td>An identifier called &lt;type> has been placed into a section of a grammar which expects a type, but &lt;type> is not a valid type
   </td>
  </tr>
  <tr>
   <td><code>Illegal function name: '&lt;function name>' !</code>
   </td>
   <td>A function has been given the name &lt;function name> which is not a valid non-type identifier. See the section on identifiers to construct a valid one 
   </td>
  </tr>
  <tr>
   <td><code>Parameter &lt;parameter name> is a duplicate!</code>
   </td>
   <td>Within a function declaration, two or more parameters share the name &lt;parameter name>
   </td>
  </tr>
  <tr>
   <td><code>Parameter name '&lt;parameter name>' is not a legal identifier!</code>
   </td>
   <td>Within a function declaration, a parameter has been given the name &lt;parameter name> which is not a valid non-type identifier. See the section on identifiers to construct a valid one
   </td>
  </tr>
  <tr>
   <td><code>Duplicate function declaration: '&lt;function name>'!</code>
   </td>
   <td>Two functions have been named &lt;function name> and have the same pattern of arguments
   </td>
  </tr>
  <tr>
   <td><code>Constants must be assigned to!</code>
   </td>
   <td>A constant has been declared in a class but has not been assigned to
   </td>
  </tr>
  <tr>
   <td><code>Cannot create a nested function!</code>
   </td>
   <td>A function has been declared inside the body of another function
   </td>
  </tr>
  <tr>
   <td><code>Brace mismatch!</code>
   </td>
   <td>An opening or closing brace does not have a proper match in the code
   </td>
  </tr>
  <tr>
   <td><code>No return statement!</code>
   </td>
   <td>A function has terminated without encountering a return statement
   </td>
  </tr>
  <tr>
   <td><code>Else without if!</code>
   </td>
   <td>An else keyword has been used without an if statement
   </td>
  </tr>
  <tr>
   <td><code>Improperly formed variable initialization!</code>
   </td>
   <td>A variable declaration has been created that does not fit the expected declaration grammar.
   </td>
  </tr>
  <tr>
   <td><code>Illegal variable name: '&lt;variable name>' !</code>
   </td>
   <td>A variable has been declared with the name &lt;variable name> which is not a valid non-type identifier. See the section on identifiers to construct a valid one.
   </td>
  </tr>
  <tr>
   <td><code>Duplicate variable declaration: '&lt;variable name>' !</code>
   </td>
   <td>A variable has been declared with &lt;variable name> but another variable with that name already exists in scope.
   </td>
  </tr>
  <tr>
   <td><code>Syntax error on if!</code>
   </td>
   <td>An if statement has been created that does not match the expected grammar.
   </td>
  </tr>
  <tr>
   <td><code>Brace mismatch on if!</code>
   </td>
   <td>An if statement has been created that has improperly matched braces.
   </td>
  </tr>
  <tr>
   <td><code>Cannot use a non-integer index in for loop!</code>
   </td>
   <td>A non-integer has been used as the index for a for loop.
   </td>
  </tr>
  <tr>
   <td><code>Cannot index an array with a non-integer!</code>
   </td>
   <td>A non-integer has been placed into an index for an array.
   </td>
  </tr>
  <tr>
   <td><code>Division by zero!</code>
   </td>
   <td>Some operation has been called which has encountered a division by zero. This may be division or modulo.
   </td>
  </tr>
  <tr>
   <td><code>Failed assertion!</code>
   </td>
   <td>The argument of an assert statement has been resolved to false.
   </td>
  </tr>
  <tr>
   <td><code>Function '&lt;function name>' is ambiguous and cannot be used in a first-class context!</code>
   </td>
   <td>Multiple functions exist with the name &lt;function name> making first class references to it impossible to disambiguate.
   </td>
  </tr>
  <tr>
   <td><code>Syntax error on expression parser!</code>
   </td>
   <td>An expression has been improperly constructed.
   </td>
  </tr>
  <tr>
   <td><code>Function '&lt;function name>' does not exist!</code>
   </td>
   <td>A function has been called with the name &lt;function name> which does not exist in scope.
   </td>
  </tr>
  <tr>
   <td><code>No recognized type for '==' !</code>
   </td>
   <td>The equality operator, ==, has been called between two types that do not support the equality operator.
   </td>
  </tr>
  <tr>
   <td><code>No recognized type for '!=' !</code>
   </td>
   <td>The inequality operator, !=, has been called between two types that do not support the inequality operator.
   </td>
  </tr>
  <tr>
   <td><code>Parentheses mismatch!</code>
   </td>
   <td>There has been a mismatch of open and close parentheses within an expression.
   </td>
  </tr>
  <tr>
   <td><code>Cannot create an array of conflicting types '&lt;original type>' and '&lt;element type>' !</code>
   </td>
   <td>An element in an array literal with the type &lt;element type> is not compatible with the type of its first element, &lt;original type>.
   </td>
  </tr>
  <tr>
   <td><code>Cannot unwrap non-array type '&lt;type>' !</code>
   </td>
   <td>An attempt has been made to get the element type of the type &lt;type> that does not have an element type.
   </td>
  </tr>
</table>


Additionally, programmers may define errors within the program by using the throw function. These errors may have arbitrary error messages, however all errors thrown by the throw function have the same error code.

