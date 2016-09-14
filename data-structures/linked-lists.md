## linked lists

#### how do linked lists work?
  * allow for sequential access only
  * data is stored anywhere in memory
  * unlike with arrays, data never has to be moved
  * each item stores the address of the next item in the list

#### upsides:
  * __insertion:__
    * simply change the address stored in the previous item.
    * __real life analogy:__ the movie theater has enough seats to accommodate you and your group of friends,
    but you can't all sit together.  y'all are cool with that.

#### downsides:
  * __reading:__
    * finding and reading data from a specific item would require, at worst, iterating over the entire linked list.

#### time complexities:
  * __reading:__ O(n) -> linear time
  * __insertion:__ O(1) -> constant time
  * __deletion:__ O(n) -> linear time (or constant time for head/tail, if either is known)

#### implementation:

```javascript
// constructor function to create new node
var Node = function(value) {
  this.value = value;
  this.next = null;
};

// constructor function to create linked list
var LinkedList = function() {
  this.head = null;
  this.tail = null;
};

LinkedList.prototype.addToTail = function(value) {
  var newTail = new Node(value);

  // if linked list had no head, list was empty
  // adding one node to an empty list makes that node both the head and the tail
  if (!this.head) {
    this.head = newTail;
  // if the list wasn't empty, the tail would exist
  // the current tail will now point to the new node
  } else {
    this.tail.next = newTail;
  }

  // reassign the linked list's tail to the new node
  this.tail = newTail;
};

LinkedList.prototype.removeHead = function() {
  // if linked list is empty, return null
  if (!this.head) {
    return null;
  }

  // save current head to variable to be returned
  var currentHead = this.head;
  // reassign value of linked list's head to the next node
  this.head = this.head.next;

  return currentHead.value;
};

LinkedList.prototype.contains = function(target) {
  // start search from head
  var currentNode = this.head;

  // keep searching until there are no nodes left
  while (currentNode) {
    // if current node's value equals the target, return true
    if (currentNode.value === target) {
      return true;
    }

    // reset the value of current node to the next node
    currentNode = currentNode.next;
  }

  // if loop ends without returning, target is not in linked list
  return false;
};
```