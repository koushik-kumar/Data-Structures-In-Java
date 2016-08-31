## Arrays

- Arrays is the most basic type of data structure that stores similar kind of values. 
- Each item in a array is a element and can be accessed using a index. 
    - Normally arrays have 0 based index which means indexing starts from 0 and goes till _n - 1_ where n is the number of elements in array.
- Size of an array is fixed at runtime when initialized. It can't be changed after initialization.
- If size has to be changed after initialization, use _ArrayList_ (Collection class) instead.
- Size of an array can be specified using int only, since arrays are int based index.
- Below is the representation, 

<img width="426" alt="screen shot 2016-08-31 at 2 21 49 pm" src="https://cloud.githubusercontent.com/assets/3439029/18146774/600b0d4a-6f86-11e6-8005-3f6da1afc95f.png">

- Java offers several ways of defining and initializing arrays, including literal and constructor notations. When declaring arrays without explicit values, each element will be initialized with a default value:
    - **0** for primitive numerical types: _byte, short, char, int, long, float, and double._
    - **false** for the _boolean_ type.
    - **null** for _reference_ types.

- In Java, it is possible to have arrays of size 0:
```java 
int[] array = new int[0]; // Compiles and runs fine.
```
   However, since it's an empty array, no elements can be assigned to it:
```java
array[0] = 1; // Throws java.lang.ArrayIndexOutOfBoundsException.
```
Such empty arrays are typically useful as return values, so that the calling code only has to worry about dealing with an array, rather than a potential null value that may lead to a NullPointerException.

The length of an array must be a non-negative integer:
```java
int[] array = new int[-1]; // Throws java.lang.NegativeArraySizeException
```
The array size can be determined using a public final field called length:
```java
System.out.println(array.length); // Prints 0 in this case.
```
**Note:** _array.length_ returns the actual size of the array and not the number of array elements which were assigned a value, unlike ArrayList#size() which returns the number of array elements which were assigned a value.