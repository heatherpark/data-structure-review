## linked lists

#### how do linked lists work?
  * allow for sequential access only.
  * data is stored anywhere in memory.
  * unlike with arrays, data never has to be moved.
  * each item stores the address of the next item in the list.

#### upsides:
  * __insertion:__
    * simply change the address stored in the previous item.
    *__real life analogy:__ the movie theater has enough seats to accommodate you and your group of friends,
    but you can't all sit together.  Y'all are cool with that.

#### downsides:
  * __reading:__
    * finding and reading data from a specific item would require, at worst, iterating over the entire linked list.

#### time complexities:
  * __reading:__ O(n) -> linear time
  * __insertion:__ O(1) -> constant time
  * __deletion:__ O(n) -> linear time (or constant time for head/tail, if either is known)