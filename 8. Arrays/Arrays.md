# Arrays

In Stensl, arrays are mutable, ordered, integer-indexable collections of elements of a particular type. In many ways, they are similar to arrays in other scripting languages. An array is built out of elements, which all share the same type and have a particular order, which is denoted by an index. The first element of the array has the index 0, the second element has the index 1, and so on. The element grab operator can be used to access a particular element from an array, like so:


```
someArray[0] // gets the first element
```


More on the element grab operator can be found in the operator section. 

Unlike some languages, elements may be added and removed from arrays. This allows for more flexibility and makes the array structure more powerful. Arrays also have more built-in properties that expand their functionality. These can be found in the array property section. 

Stensl arrays may hold values of any type, including functions, objects, and other arrays. Arrays which contain other arrays are called multi-dimensional arrays as per the standard. 
