# Kotlin Cheat Sheet for paper coding
## Basic
### Class
```javascript
// Declare
class Node(
  public val value: Int,
  public var next: Node
)
val node = Node(1, null) // Initialise Node
node.next = Node(2, null) // Set to variable property

// Declare data class
data class Pos(val x: Int, val y: Int)

```
### Iterator
```javascript
// For loop
for (i in 0 until 5) {
  print(i)
}

// For in Collections: String, ArrayList, List, Array, Set
collection.forEach {
  print(it)
}
collection.forEach { c ->
  print(c)
}
collections.forEach(::print)

// For in Map
val map = mapOf(1 to "1", 2 to "2")
map.forEach{
  print("${it.key} ${it.value}")
}
map.forEach{ key, value ->
  print("$key $value")
}
```

## Collections

### Basic Functions

### String
```javascript
// Initialise
val str: String = "hello_world"

// String length
val lengthOfStr: Int = str.length

// Get Char At
val c: Char = str.get(0)
val c: Char = str[0]

// Check empty, blank, null
val isEmpty: Boolean = str?.isEmpty()
val isNullOrEmpty: Boolean = str?.isNullOrEmpty()
val isBlank: Boolean = str?.isBlank()
val isNotEmpty: Boolean = str?.isNotEmpty()

// String template
val num = 1
val list = listOf(1, 2, 3)
val str = "num = $num" // "num = 1"
val str = "list size = ${list.size}" // "list size = 3"
```

### Array, List, ArrayList
```javascript
// Initialise
val list: MutableList<String> = mutableListOf<String>("1", "2")
val array: Array<String> = arrayOf<String>("1", "2")
val arrayList: ArrayList<String> = arrayListOf<String>("1", "2")

// Get size, Apply for All
val size = colection.size

// Get item, Apply for All
val item = collection.get(0)
val item = collection[0]

// Add new item, Apply for only List and ArrayList
list.add("3") // ["1", "2", "3"]
list.add(0, "0") // ["0", "1", "2"]

arrayList.add("3")
arrayList.add(0, "3")

// Set Item, Apply for All
collection.set(0, "2") // ["2", "2"]
collection[0] = "2"

// Sorted, Apply for All, Using two pivot quick sort
val sortedList: List<String> = collection.sorted()

```
### Map
```javascript
// Initialise
val map = hashMapOf('c' to "CCC", 'b' to "BBB")
```

### Stack, ArrayDeque
*Note*: ArrayDeque is faster than Stack
```javascript
// Import
import java.util.Stack
import java.util.ArrayDeque

val stack = Stack<String>() // Initialise
val peekValue = stack.peek() // Peek
val popValue = stack.pop() // Pop
stack.push("111") // Push
stack.isNotEmpty() // Check if empty
stack.size // Get size of stack

val deque = ArrayDeque<Int>()
val deque = ArrayDeque<Int>().apply {
  this.push(1)
  this.push(2)
  this.push(3)
}
val peekValue = deque.peek() // Peek, return 3
val peekFirst = deque.peekFirst() // Peak First Value, return 3
val peekLast = deque.peekLast() // Peek Last value, return 1
val first = deque.first // return 3
val last = deque.last // return 1
val popValue = deque.pop() // pop
deque.push(4) // Push [4, 3, 2, 1]
deque.add(4) // Add to Last [3, 2, 1, 4]
deque.addLast(4) // Add to Last [3, 2, 1, 4]
deque.addFirst(4) // Add to First [4, 3, 2, 1]
```


### Two dimension
### Convert
```javascript
// List to Typed list
val list: List<Int> = listOf<Int>(1, 2)
val array: Array<Int> = list.toTypedArray()
val array: IntArray = list.toIntArray()
```
