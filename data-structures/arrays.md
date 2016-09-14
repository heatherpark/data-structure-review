## arrays

#### how do arrays work?
  * allow for both random and sequential access.
  * data is stored contiguously.
  * typically, their lengths are predetermiend by the user.

#### upsides:
  * __reading:__
    * able to instantly access any item if its index is know.

#### downsides:
  * __space:__
    * not using all slots in array will result in wasted memory
  * __insertion/deletion:__
    * insertion/deletion for any slots other than the last one will cause a shift in all subsequent elements
    * insertion may require more slots than there are in the array, so all elements will have to be transferred
      to a new, more accommodating, array
      *__real life analogy:__ the movie theater has enough seats to accommodate you and your group of friends,
      but you'd have to split up, and your friends don't want to do that.

#### time complexities:
  * __reading:__ O(1) -> constant time
  * __insertion:__ O(n) -> linear time
  * __deletion:__ O(n) -> linear time
