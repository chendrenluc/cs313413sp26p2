TestIterator.java:
1: Iterating over an ArrayList (or a LinkedList) gives the same sequence of values.
The interface behaves the same for both list types, the only difference was the
performance.
2: Using i.remove removes the element that was just given by the iterator,
which is the safe way to remove items while iterating.
Using list.remove(inter.valueOf(x)) inside an iterator causes an error because it
changes the contents of the list outside the iterator instead of inside it.
3: The average was calculated using an iterator and a while loop, which gave an average of 61.3....

TestList.java:
Contains: Before adding 77 contains is false, and afterwards it is true
AddMultiple/2: Adding repeated values updates the size, indexOf, and lastIndexOf, which
also changes any method that accesses an element with get.
Remove vs Remove(Object): list.remove(5) removes the element at the index of 5,
list.remove(Integer.valueOf(5)) removes the first 5 it finds in the list.
All: containsAll checks whether all elements in a given collection appear at least once in the list.
addAll adds or appends an entire collection of integers in one function.
removeAll does the opposite of addAll, in one function.
And retainAll iterates through the list and removes everything except the elements that
match the given collection input.
Set: The set method replaces values at specific indices without changing the list size,
it just replaces whatever is there already.
SubList: Returns a view of the list starting at the index (the first input) and going to the end (last input).

TestPerformance.java:
Observations:
AddRemove at index of 0; LinkedList is slightly faster, because the bigO for the head is 0(1)
and for ArrayList it is 0(n).
Get; ArrayList is way faster, because it is built to support random access and the Linkedlist has to travel the nodes