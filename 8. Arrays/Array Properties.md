## Array Properties

Currently, all the properties implemented for arrays are functions. These functions provide various necessary and helpful utilities. These functions may not be used from a first class context because they are implemented on a lower level than Stensl for performance reasons.


### length

The length property of an array is a function which returns the number of elements that it contains. It takes no arguments. It returns an integer. It may be called like so:


```
someArray.length() // gets array length
```



### add

The add property of an array is a function which appends a new element to the end of the array. It takes one argument, which must have a compatible type of the elements of the array. That argument is the element that is added onto the array. It returns void. It may be called like so:


```
someIntArray.add(5) // adds '5' onto the end of the array
```



### remove

The remove property of an array is a function which removes the element that lies at a particular index within that array. It takes one argument, which is the index of the element to remove. This argument must be an integer and it must be a valid index of the array; it must be non-negative and less than the number of elements of the array. It returns void. The function may be called like so:


```
someIntArray.remove(5) // removes the fifth element of the array
```



### rotate

The rotate property of an array is a function which shifts the elements of an array. It takes one argument, which must be an integer, which determines the shift amount. Once rotate is called, each element of the array which previously lay at some index can afterwards be found at the index defined by (previous index + shift amount) % array length, where “%” is the modulo operator. For instance, for an array containing the elements 1,2,3,4,5 in order, a call to the rotate function with the shift amount 2 would change the array to now contain 4,5,1,2,3. It returns void. The function may be called like so:


```
someIntArray.remove(5) // removes the fifth element of the array
```
