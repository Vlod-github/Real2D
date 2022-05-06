# Real 2D
This cjass library provides a Real2D structure that provides methods for working with a 2D array of floats. All methods contain TriggerSleepAction() interrupts to protect against thread breakage. All methods use cycles from 1 to length and from 1 to width, keep this in mind. The library uses a native hashtable to store elements and is dependent on the [HT library](https://github.com/Vlod-github/Risk-free-creation-of-hashtable/blob/master/source/HT.vjass)
## API
```scala
// Create. length and width of the matrix
Real2D map = Real2D.create(integer length, integer width)

// Delete an object
map.destroy()

// Read value. a, b - indexes
real value = map.getr(integer a, integer b)

// Write value
map.setr(integer a, integer b, real value)

// Make a copy
Real2D newmap = map.copy()

// Find the maximum and minimum element
map.maxmin()
real max = map.max
real min = map.min

// Normalization (bringing all numbers into the range [0,1])
map = map.norm() // returns the same object

// Multiply each element of a matrix by a number
map = map.multiply(real number) // returns the same object


// Raise each element to a degree
map = map.pow(real degree) // returns the same object

// Square each element
map = map.square() // returns the same object
```