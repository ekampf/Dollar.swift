Dollar and Cent
===========

![Introducing Dollar and Cent](https://raw.githubusercontent.com/ankurp/Dollar.swift/master/assets/hero.png)

Dollar is a Swift library that provides useful functional programming helper methods without extending any built in objects. It is similar to Lo-Dash or Underscore in Javascript.

Cent is a library that extends certain Swift object types using the extension feature and gives its two cents to Swift language.

## Contents ##

- [Setup](#setup)
- Dollar
  - [Usage](#dollar-usage)
    - [Array](#array-methods)
    - [Dictionary](#dictionary-methods)
    - [Object](#object-methods)
    - [Function](#function-methods)
    - [Chaining](#chaining)
  - [Examples](#dollar-examples)
    - [Array](#array)
    - [Dictionary](#dictionary)
    - [Object](#object)
    - [Function](#function)
    - [Chaining](#chaining---array-)
- Cent
  - [Usage](#cent-usage)
    - [Array](#array-extensions)
    - [Date](#date-extensions)  
    - [Dictionary](#dictionary-extensions)
    - [Int](#int-extensions)
    - [String](#string-extensions)
    - [Range](#range-extensions)
  - [Examples](#cent-examples)
    - [Array](#array-example-usage)
    - [Date](#date-example-usage)
    - [Dictionary](#dictionary-example-usage)
    - [Int](#int-example-usage)
    - [String](#string-example-usage)
    - [Range](#range-example-usage)
- [Contributing](#contributing)
- [Roadmap](#roadmap)
- [Dollar or Cent?](#dollar-or-cent)

## Setup ##

Currently there are issues loading the library using `pod 'Dollar'` which is pending changes from Cocoapods. In the mean time follow these steps

1. If you are using git then add Dollar as a submodule using `git submodule add https://github.com/ankurp/Dollar.swift.git` otherwise download the project using `git clone https://github.com/ankurp/Dollar.swift.git` in your project folder.
2. Open the Dollar.swift folder. Drag Dollar.xcodeproj, inside the Dollar folder, into the file navigator of your Xcode project.
3. In Xcode, navigate to the target configuration window by clicking on the blue project icon, and selecting the application target under the "Targets" heading in the sidebar.
4. In the tab bar at the top of that window, open the "Build Phases" panel.
5. Expand the "Link Binary with Libraries" group, and add Dollar.framework.
6. In your project file `import Dollar` and you can call all of the helper functions.

![How to import library](https://raw.githubusercontent.com/ankurp/Dollar.swift/master/assets/HowToImport.gif)

## Dollar Usage ##

### Array Methods ###

Method | Usage
---- | ---------
**`$.at`**|Creates an array of elements from the specified indexes, or keys, of the collection. Indexes may be specified as individual arguments or as arrays of indexes.
**`$.compact`**|Creates an array with all nil values removed.
**`$.contains`**|Checks if a given value is present in the array.
**`$.difference`**|Creates an array excluding all values of the provided arrays
**`$.every`**|Checks if the given callback returns true value for all items in the array.
**`$.find`**|Iterates over elements of an array and returning the first element that the callback returns true for.
**`$.findIndex`**|This method is like find except that it returns the index of the first element that passes the callback check.
**`$.findLastIndex`**|This method is like findIndex except that it iterates over elements of the array from right to left.
**`$.first`**|Gets the first element in the array.
**`$.second`**|Gets the second element in the array.
**`$.third`**|Gets the third element in the array.
**`$.flatten`**|Flattens a nested array of any depth.
**`$.frequencies`**|This method returns a dictionary of values in an array mapping to the total number of occurrences in the array. If passed a function it returns a frequency table of the results of the given function on the arrays elements.
**`$.indexOf`**|Gets the index at which the first occurrence of value is found.
**`$.initial`**|Gets all but the last element or last n elements of an array.
**`$.intersection`**|Creates an array of unique values present in all provided arrays.
**`$.join`**|Joins the elements in the array to create a concatenated element of the same type.
**`$.last`**|Gets the last element from the array.
**`$.lastIndexOf`**|Gets the index at which the last occurrence of value is found.
**`$.rest`**|The opposite of initial this method gets all but the first element or first n elements of an array.
**`$.max`**|Retrieves the maximum value in an array.
**`$.merge`**|Creates an array of all values, including duplicates, of the arrays in the order they are provided.
**`$.min`**|Retrieves the minimum value in an array.
**`$.pluck`**|Retrieves the value of a specified property from all elements in the array.
**`$.pull`**|Removes all provided values from the given array.
**`$.range`**|Creates an array of numbers (positive and/or negative) progressing from start up to but not including end.
**`$.sequence`**|Creates an array of an arbitrary sequence. Especially useful with builtin ranges.
**`$.remove`**|Removes all elements from an array that the callback returns true.
**`$.shuffle`**|Shuffles and returns the new shuffled array.
**`$.slice`**|Slices the array based on the start and end position. If an end position is not specified it will slice till the end of the array.
**`$.sortedIndex`**|Gives the smallest index at which a value should be inserted into a given the array is sorted.
**`$.union`**|Creates an array of unique values, in order, of the provided arrays.
**`$.uniq`**|Creates a duplicate-value-free version of an array.
**`$.without`**|Creates an array excluding all provided values.
**`$.xor`**|Creates an array that is the symmetric difference of the provided arrays.
**`$.zip`**|Creates an array of grouped elements, the first of which contains the first elements of the given arrays.
**`$.zipObject`**|Creates an object composed from arrays of keys and values.
**`$.partition`**|Produces an array of arrays, each containing n elements, each offset by step. Stops after a partition is less than n length.
**`$.partitionAll`**|Produces an array of arrays, each containing n elements, each offset by step. Continues after a partition is less than n length.
**`$.partitionBy`**|Applies a function to each element in array, splitting it each time the function returns a new value.


### Dictionary Methods ###

Method | Usage
---- | ---------
**`$.keys`**|Creates an array of keys given a dictionary.
**`$.values`**|Creates an array of values given a dictionary
**`$.merge`**|Merges all of the dictionaries together and the latter dictionary overrides the value at a given key
**`$.pick`**|Creates a shallow clone of a dictionary composed of the specified keys.
**`$.omit`**|Creates a shallow clone of a dictionary excluding the specified keys.

### Object Methods ###

Method | Usage
---- | ---------
**`$.tap`**|Invokes interceptor with the object and then returns object.

### Function Methods ###

Method | Usage
---- | ---------
**`$.after`**|Creates a function that executes passed function only after being called n times.
**`$.bind`**|Creates a function that, when called, invokes func with the binding of arguments provided.
**`$.id`**|The identify function which simply returns the argument its given.
**`$.memoize`**|Returns a memoized function to improve performance by caching recursive function values.
**`$.noop`**|A no-operation function.
**`$.partial`**|Creates a function that, when called, invokes func with any additional partial arguments prepended to those provided to the new function.
**`$.times`**|Call a function n times and also passes the index. If a value is returned in the function then the times method will return an array of those values.

### Chaining ###

**`$(array: ...)`**

Method | Usage
---- | ---------
**`any`**|Returns true if callback function returns true for at least one element in the array
**`all`**|Returns true if callback function returns true for all elements in the array
**`each`**|Passes each element value to the callback function
**`filter`**|Filters the arrary to elements for which the callback function returns true
**`first`**|Returns the first element in the array and terminated the chain
**`second`**|Returns the second element in the array and terminated the chain
**`third`**|Returns the third element in the array and terminated the chain
**`flatten`**|Flattens a nested array of any depth.
**`initial`**|Gets all but the last element or last n elements of an array.
**`map`**|Maps each element to the new value returned in the callback function
**`slice`**|Slices the array based on the start and end position. If an end position is not specified it will slice till the end of the array.
**`value`**|Returns the value after evaluating all callbacks

## Dollar Examples ##

### Array ###

### at - `$.at`

Creates an array of elements from the specified indexes, or keys, of the collection. Indexes may be specified as individual arguments or as arrays of indexes.

```swift
$.at(["ant", "bat", "cat", "dog", "egg"], indexes: 0, 2, 4) 
=> ["ant", "cat", "egg"]
```

### compact - `$.compact`

Creates an array with all nil values removed.

```swift
$.compact([3, nil, 4, 5]) 
=> [3, 4, 5]

$.compact([nil, nil]) as NSObject[] 
=> []
```

### contains - `$.contains`

Checks if a given value is present in the array.

```swift
$.contains([1, 2, 3, 1, 2, 3], value: 2) 
=> true

$.contains([1, 2, 3, 1, 2, 3], value: 10) 
=> false
```

### difference - `$.difference`

Creates an array excluding all values of the provided arrays

```swift
$.difference([1, 2, 3, 4, 5], [5, 2, 10]) 
=> [1, 3, 4]
```


### every - `$.every`

Checks if the given callback returns true value for all items in the array.

```swift
$.every([1, 2, 3, 4], iterator: { $0 < 20 }) 
=> true

$.every([1, 2, 3, 4]) { $0 == 1 } 
=> false
```

### find - `$.find`

Iterates over elements of an array and returning the first element that the callback returns true for.

```swift
$.find([1, 2, 3, 4], iterator: { $0 == 2 }) 
=> 2

$.find([1, 2, 3, 4]) { $0 == 10 } 
=> nil
```

### findIndex - `$.findIndex`

This method is like find except that it returns the index of the first element that passes the callback check.

```swift
let arr = [["age": 36], ["age": 40], ["age": 1]]
let result = $.findIndex(arr) { $0["age"] < 20 }
result 
=> 2
```

### findLastIndex - `$.findLastIndex`

This method is like findIndex except that it iterates over elements of the array from right to left.

```swift
let arr = [["age": 36], ["age": 40], ["age": 1]]
let result = $.findLastIndex(arr) { $0["age"] > 30 }
result
=> 1
```

### first - `$.first(array: AnyObject[])`

Gets the first element in the array.

```swift
$.first([1, 2, 3, 4])
=> 1

$.first([]) 
=> nil
```

### second - `$.second(array: AnyObject[])`

Gets the second element in the array.

```
$.second([1, 2, 3, 4])
=> 2

$.second([1]) 
=> nil

$.second([])
=> nil
```

### flatten - `$.flatten`

Flattens a nested array of any depth.

```swift
$.flatten([[3], 4, 5]) as Int[] 
=> [3, 4, 5]

$.flatten([[3], "Hello", 5]) as NSObject[] 
=> [3, "Hello", 5]

$.flatten([[[3], 4], 5]) as Int[] 
=> [3, 4, 5]
```

### frequencies - `$.frequencies`
This method returns a dictionary of values in an array mapping to the total number of occurrences in the array. If passed a function it returns a frequency table of the results of the given function on the arrays elements.

```swift
$.frequencies(["a", "a", "b", "c", "a", "b"]) 
=> ["a": 3, "b": 2, "c": 1]

$.frequencies([1, 2, 3, 4, 5]) { $0 % 2 == 0 }
=> [false: 3, true: 2]
```

### indexof - `$.indexof`

Gets the index at which the first occurrence of value is found.

```swift
$.indexOf([1, 2, 3, 1, 2, 3], value: 2) 
=> 1

$.indexOf(["A", "B", "C"], value: "B") 
=> 1

$.indexOf([3, 4, 5], value: 5) 
=> 2

$.indexOf([3, 4, 5], value: 3) 
=> 0

$.indexOf([3, 4, 5], value: 2) 
=> nil
```

### initial - `$.initial`

Gets all but the last element or last n elements of an array.

```swift
$.initial([3, 4, 5]) 
=> [3, 4]

$.initial([3, 4, 5], numElements: 2) 
=> [3]
```

### intersection - `$.intersection`

Creates an array of unique values present in all provided arrays.

```swift
$.intersection([1, 2, 3], [5, 2, 1, 4], [2, 1]) 
=> [1, 2]
```

### last - `$.last`

Gets the last element from the array.

```swift
$.last([3, 4, 5]) 
=> 5
```

### lastIndexOf - `$.lastIndexOf`

Gets the index at which the last occurrence of value is found.

```swift
$.lastIndexOf([1, 2, 3, 1, 2, 3], value: 2) 
=> 4
```

### rest - `$.rest`

The opposite of initial this method gets all but the first element or first n elements of an array.

```swift
$.rest([3, 4, 5]) 
=> [4, 5]

$.rest([3, 4, 5], numElements: 2) 
=> [5]
```

### min - `$.min`

Retrieves the minimum value in an array.

```swift
$.min([2, 1, 2, 3, 4]) 
=> 1
```

### max - `$.max`

Retrieves the maximum value in an array.

```swift
$.max([1, 2, 3, 4, 2, 1]) 
=> 4
```

### pluck - `$.pluck`

Retrieves the value of a specified property from all elements in the array.

```swift
let arr : Dictionary<String, Int>[] = [["age": 20], ["age": 30], ["age": 40]]
$.pluck(arr, value: "age") 
=> [20, 30, 40]
```

### pull - `$.pull`

Removes all provided values from the given array.

```swift
$.pull([3, 4, 5, 3, 5], values: 3, 5) 
=> [4]

$.pull([3, 4, 5, 3, 5], values: 4) 
=> [3, 5, 3, 5]

$.pull([3, 4, 5, 3, 5], values: 3, 4, 5) 
=> []
```

### range - `$.range`

Creates an array of numbers (positive and/or negative) progressing from start up to but not including end.

```swift
$.range(4) 
=> [0, 1, 2, 3]

$.range(1, endVal: 5) 
=> [1, 2, 3, 4]

$.range(0, endVal: 20, incrementBy: 5) 
=> [0, 5, 10, 15]
```

### sample - `$.sample`
```
let arr : Int[] = [2, 1, 2, 3, 4]
$.contains(arr, value: $.sample(arr))
=> true
```

### sequence - `$.sequence`

Creates an array of an arbitrary sequence. Especially useful with builtin ranges.

```swift
$.sequence(0..4) 
=> [0, 1, 2, 3]

$.sequence(-2.0..2.0) 
=> [-2.0, -1.0, 0.0, 1.0]

$.sequence((0..20).by(5)) 
=> [0, 5, 10, 15]

$.sequence("abc") 
=> ["a", "b", "c"]
```

### remove - `$.remove`

Removes all elements from an array that the callback returns true.

```swift
let result = $.remove([1, 2, 3, 4, 5, 6]) { $0 == 2 || $0 == 3 }
result
=> [1, 4, 5, 6]
```

### shuffle - `$.shuffle`

Shuffles and returns the new shuffled array

```swift
let result = $.shuffle([1, 2, 3, 4, 5, 6])
result
=> [4, 1, 3, 5, 6, 2]
```

### sortedIndex - `$.sortedIndex`

Gives the smallest index at which a value should be inserted into a given the array is sorted.

```swift
$.sortedIndex([3, 4, 6, 10], value: 5)
=> 2

$.sortedIndex([10, 20, 30, 50], value: 40)
=> 3
```

### union - `$.union`

Creates an array of unique values, in order, of the provided arrays.

```swift
$.union([1, 2, 3], [5, 2, 1, 4], [2, 1]) 
=> [1, 2, 3, 4, 5]
```

### merge - `$.merge`

Creates an array of all values, including duplicates, of the arrays in the order they are provided.

```swift
let arr  = [1, 5]
let arr2 = [2, 4]
let arr3 = [5, 6]
let result = $.merge(arrays: arr, arr2, arr3)
result
=> [1, 5, 2, 4, 5, 6]
```

### uniq - `$.uniq`

Creates a duplicate-value-free version of an array.

```swift
$.uniq([1, 2, 1, 3, 1])
=> [1, 2, 3]
```

### without - `$.without`

Creates an array excluding all provided values.

```swift
$.without([3, 4, 5, 3, 5], values: 3, 5)
=> [4]

$.without([3, 4, 5, 3, 5], values: 4)
=> [3, 5, 3, 5]

$.without([3, 4, 5, 3, 5], values: 3, 4, 5)
=> []
```

### xor - `$.xor`

Creates an array that is the symmetric difference of the provided arrays.

```swift
$.xor([1, 2, 3], [5, 2, 1, 4])
=> [3, 4, 5]
```

### zip - `$.zip`

Creates an array of grouped elements, the first of which contains the first elements of the given arrays.

```swift
$.zip(["fred", "barney"], [30, 40], [true, false]) as NSObject[] 
=> [["fred", 30, true], ["barney", 40, false]]
```

### zipObject - `$.zipObject`

Creates an object composed from arrays of keys and values.

```swift
$.zipObject(["fred", "barney"], values: [30, 40]) as Dictionary<String, Int> 
=> ["fred": 30, "barney": 40]
```

### partition - `$.partition`

Produces an array of arrays, each containing n elements, each offset by step. Stops after a partition is less than n length.

```swift
let arr = [1, 2, 3, 4, 5]
$.partition(arr, n: 2)
=> [[1, 2], [3, 4]]

$.partition(arr, n: 4, step: 1)
=> [[1, 2, 3, 4], [2, 3, 4, 5]]

$.partition(arr, n: 4, step: 1, pad: nil)
=> [[1, 2, 3, 4], [2, 3, 4, 5], [3, 4, 5]]

$.partition(arr, n: 4, step: 1, pad: [6, 7, 8])
=> [[1, 2, 3, 4], [2, 3, 4, 5], [3, 4, 5, 6]]
```

### partitionAll - `$.partitionAll`

Produces an array of arrays, each containing n elements, each offset by step. Continues after a partition is less than n length.

```swift
$.partitionAll([1, 2, 3, 4, 5], n:4, step: 1)
=> [[1, 2, 3, 4], [2, 3, 4, 5], [3, 4, 5], [4, 5], [5]]
```

### partitionBy - `$.partitionBy`

Applies a function to each element in array, splitting it each time the function returns a new value.

```swift
$.partitionBy([1, 2, 3, 4, 5]) { $0 % 2 == 0 }
=> [[1], [2, 4], [3, 5], [6]]

$.partitionBy([1, 7, 3, 6, 10, 12]) { $0 % 3 }
=> [[1, 7], [3, 6], [10], [12]]
```

### Dictionary ###

### keys - `$.keys`

Creates an array of keys given a dictionary.

```swift
$.keys(["Dog": 1, "Cat": 2])
=> ["Dog", "Cat"]
```

### values - `$.values`

Creates an array of values given a dictionary

```swift
$.values(["Dog": 1, "Cat": 2])
=> [1, 2]
```

### merge - `$.merge`

Merges all of the dictionaries together and the latter dictionary overrides the value at a given key

```swift
let dict: Dictionary<String, Int> = ["Dog": 1, "Cat": 2]
let dict2: Dictionary<String, Int> = ["Cow": 3]
let dict3: Dictionary<String, Int> = ["Sheep": 4]
$.merge(dictionaries: dict, dict2, dict3)
=> ["Dog": 1, "Cat": 2, "Cow": 3, "Sheep": 4]
```

### pick - `$.pick`

Creates a shallow clone of a dictionary composed of the specified keys.

```swift
$.pick(["Dog": 1, "Cat": 2, "Cow": 3], keys: "Dog", "Cow")
=> ["Dog": 1, "Cow": 3]
```

### omit - `$.omit`

Creates a shallow clone of a dictionary excluding the specified keys.

```swift
$.omit(["Dog": 1, "Cat": 2, "Cow": 3], keys: "Cat", "Dog")
=> ["Cow": 3, "Sheep": 4]
```

### Object ###

### tap - `$.tap`

Invokes interceptor with the object and then returns object.

```swift
var beatle = Car(name: "Fusca")
$.tap(beatle, {$0.name = "Beatle"}).color = "Blue"
```

### Function ###

### after - `$.after`

Creates a function that executes passed function only after being called n times.

```swift
var saves = ["profile", "settings"];
let asyncSave = { (function: () -> ()?) in
   function() // Saving right away for testing but in real world would be async
}
var isDone = false
var completeCallback = $.after(saves.count) {
   isDone = true
}
for elem in saves {
   asyncSave(completeCallback)
}
isDone 
=> true
```

### bind - `$.bind`

Creates a function that, when called, invokes func with the binding of arguments provided.

```swift
let helloWorldFunc = $.bind({(T...) in T[0] + " " + T[1] + " from " + T[2] }, "Hello", "World", "Swift")
helloWorldFunc() 
=> "Hello World from Swift"
```

### id - `$.id`

The identify function which simply returns the argument its given.

```swift
$.id("Hello World from Swift")
=> "Hello World from Swift"
```

### memoize - `$.memoize`

Returns a memoized function to improve performance by caching recursive function values.

```swift
var times = 0 // to test memoization

let fibMemo = $.memoize { (fib: (Int -> Int), val: Int) -> Int in
times += 1
return val == 1 || val == 0 ? 1 : fib(val - 1) + fib(val - 2)
}

let x = fibMemo(5)
times
=> 6

times = 0
let y = fibMemo(5)
times
=> 0

times = 0
let z = fibMemo(6)
times
=> 1
```

### noop - `$.noop()`

A no-operation function.

```swift
$.noop() 
=> nil
```

### partial - `$.partial`

Creates a function that, when called, invokes func with any additional partial arguments prepended to those provided to the new function.

```swift
let partialFunc = $.partial({(T...) in T[0] + " " + T[1] + " from " + T[2] }, "Hello")
partialFunc("World", "Swift") 
=> "Hello World from Swift"
```

### times - `$.times`

Call a function n times and also passes the index. If a value is returned in the function then the times method will return an array of those values.

```swift
let fun = $.bind({ (names: String...) -> String in
   let people = $.join(names, separator: " from ")
   return "Hello \(people)"
   }, "Ankur", "Swift")
$.times(2, function: fun) as String[] 
=> ["Hello Ankur from Swift", "Hello Ankur from Swift"]
```

### Chaining - `$(array: ...)`
```swift
$(array: [1, 2, 3])

$(array: [1, 2, 3]).first().value()! as Int 
=> 1

$(array: [[1, 2], 3, [[4], 5]]).flatten().initial(2).value()! as Int[] 
=> [1, 2, 3]

$(array: [[1, 2], 3, [[4], 5]]).initial().flatten().first().value()! as Int 
=> 1

var chain = $(array: [10, 20, 30, 40, 50])
var elements: Int[] = []
chain.each { elements += $0 as Int }
elements as Int[] 
=> [10, 20, 30, 40, 50]

var chain = $(array: [10, 20, 30, 40, 50])
chain.all({ ($0 as Int) < 100 }).value()! as Bool
=> true

chain.all({ ($0 as Int) < 40 }).value()! as Bool
=> false

chain.any({ ($0 as Int) < 40 }).value()! as Bool
=> true
```


## Cent Usage ##

### Array Extensions ###

Method | Usage
---- | ---------
**`at(indexes: Int...) -> [Element]`**| Creates an array of elements from the specified indexes, or keys, of the collection.
**`every(iterator: (Element) -> Bool) -> Bool`**| Checks if the given callback returns true value for all items in the array.
**`findIndex(iterator: (Element) -> Bool) -> Int?`**| This method is like find except that it returns the index of the first element that passes the callback check.
**`findLastIndex(iterator: (Element) -> Bool) -> Int?`**| This method is like findIndex except that it iterates over elements of the array from right to left.
**`first() -> Element?`**| Gets the first element in the array.
**`flatten() -> [Element]`**| Flattens a nested array of any depth.
**`get(index: Int) -> Element?`**| Get element at index
**`initial(numElements: Int? = 1) -> [Element]`**| Gets all but the last element or last n elements of an array.
**`last() -> Element?`**| Gets the last element from the array.
**`rest(numElements: Int? = 1) -> [Element]`**| The opposite of initial this method gets all but the first element or first n elements of an array.
**`min<T: Comparable>() -> T?`**| Retrieves the minimum value in an array.
**`max<T: Comparable>() -> T?`**| Retrieves the maximum value in an array.

### Date Extensions ###

Method | Usage
---- | ---------
**`Date.from(#year: Int, month: Int, day: Int) -> NSDate`**| Returns a new Date given the year month and day
**`Date.parse(dateStr: String, format: String = "yyyy-MM-dd") -> NSDate`**| Parses the date based on the format and return a new Date
**`Date.unix(date: NSDate = NSDate()) -> Double`**| Returns the unix timestamp of the date passed in or the current unix timestamp

### Dictionary Extensions ###

Method | Usage
---- | ---------
**`isEmpty () -> Bool`**| Checks whether Dictionary has no keys and hence is empty
**`merge<K, V>(dictionaries: Dictionary<K, V>...)`**| Merges the dictionary with dictionaries passed. The latter dictionaries will override values of the keys that are already set

### Int Extensions ###

Method | Usage
---- | ---------
**`times(callback: (Int) -> ())`**| Invoke a callback n times with callback that takes index
**`times (function: () -> ())`**| Invoke a callback n times

### String Extensions ###

Method | Usage
---- | ---------
**`[i: Int] -> Character?`**| Get character at a subscript
**`[r: Range<Int>] -> String`**| Get substring using subscript notation and by passing a range
**`split(delimiter: Character) -> [String]`**| Get an array from string split using the delimiter character

### Range Extensions ###

Method | Usage
---- | ---------
**`eachWithIndex(callback: (T) -> ())`**| For each index in the range invoke the callback by passing the item in range
**`each(callback: () -> ())`**| For each index in the range invoke the callback
**`==`**| Check the equality of two ranges

## Cent Examples ##

### Array Example Usage ###
```swift
let array = ["foo", "spam", "bar", "eggs"]
let some = array.at(1, 3)
=> ["spam", "eggs"]

["angry", "hungry"].every { (a: String) -> (Bool) in a.hasSuffix("gry") }
=> true

let ind: int? = ["foo", "bar", "spam", "eggs"].findIndex({ $0.length == 4 })
ind! == 2 
=> true

let ind: int? = ["foo", "bar", "spam", "eggs"].findLastIndex({ $0.length == 4 })
ind! == 3 
=> true

let first = ["foo", "bar"].first()
=> "foo"

let unFlattened = ["foo", ["bar"], [["spam"]], [[["eggs"]]] ]
let flattened = unFlattened.flatten() 
=> ["foo", "bar", "spam", "eggs"]

let element = ["foo", "bar"].get(0)
element!
=> "foo"

let nothing = ["foo", "bar"].get(1000)
=> nil

let initial = ["foo", "bar", "spam"].initial(2) 
=> ["foo"]

let last = ["foo", "bar"].last() 
=> "bar"

let rest = ["foo", "bar", "spam"].rest(2)
=> ["spam"]

let min = [ 0, 1, 2 ].min()
=> 0

let max = [ 0, 1, 2].max()
=> 2
```

### Date Example Usage ###
```swift
let date = Date.from(2014, 1, 1) 
=> "Jan 1, 2014, 12:00 AM"

let parsedDate = Date.parse("2014-01-01", format: "yyyy-MM-dd")
=> "Jan 1, 2014, 12:00 AM"

let currentUnix = Date.unix()
=> 1,412,829,874.07114

var otherNSDate = Date()
let otherUnix = Date.unix(otherDate)
=> 1,412,829,938.92399
```

### Dictionary Example Usage ###
```swift
let dictionary = [String: String]()
dictionary.isEmpty() 
=> true

["foo": "bar"].isEmpty() 
=> false

var dic = ["foo": "bar"] 
let anotherDic = ["foo": "baz", "spam": "eggs"]
dic.merge(anotherDic)
=> ["foo": "baz", "spam": "eggs"]
```

### Int Example Usage ###
```swift
5.times { print("Na") } 
=> NaNaNaNaNa

5.times { (a: Int) -> () in print("\(a) ") } 
=> 0 1 2 3 4  
```

### String Example Usage ###
```swift
"Hello World"[6] == "W"
=> true

"Hello World"[0..<5] == "Hello" 
=> true

"Hello World".split(" ") 
=> ["Hello", "World"]

"Hi"[5]
=> nil
```

### Range Example Usage ###
```swift
(1...5).eachWithIndex { (a: Int) -> () in print("\(a)") } 
=> 12345

(1...5).each { print('Na') } 
=> NaNaNaNaNa

(1...5) == (1...5) 
=> true

(1..<5) == (1...5) 
=> false
```

## Contributing ##
If you are interested in contributing checkout [CONTRIBUTING.md](CONTRIBUTING.md)

## Roadmap ##

* More functions such as curry function and then ability to lazily evaluate chained expressions.
* Add extention functions to the Cent library


### Dollar or Cent ###
If you are interested only in pure functional programming `import Dollar` otherwise `import Cent` which includes extensions for certain object type such as Array for now but more will be added.
