# Activities

## Task 1

> Refer to the following links while discussing the answer.

- What is the difference between `array` and `std::array`
  https://stackoverflow.com/questions/30263303/stdarray-vs-array-performance
  the answer:
  What are the advantages of using std::array over usual ones?
  It has friendly value semantics, so that it can be passed to or returned from functions by value. Its interface makes it more convenient to find the size, and use with STL-style iterator-based algorithms.
  Is it more performant ?
  It should be exactly the same. By definition, it's a simple aggregate containing an array as its only member.
  Just easier to handle for copy/access ?
  Yes.

- What is the difference between `std::array` and `std::vector`
  https://www.softwaretestinghelp.com/arrays-in-stl/
  the answer: static arrays have a fixed size. If in the middle of the program we have to store more elements in the array, then it becomes impossible and we are sure to get ‘out_of_bound’ exception, the moment we attempt to store elements beyond the array limits.One solution for this is having the array declared with the maximum capacity so that we will not find any problem in storing more elements at runtime. But this arrangement has a serious disadvantage in that i.e. we are wasting too much memory.
  The answer to all these issues is using a dynamic array that will expand on its own as the need arises. STL provides this dynamic array in the form of a vector container.

  Vectors are dynamic array containers that resize it automatically when elements are inserted or deleted. Storage of vector is handled by the vector container itself.
  The elements in the vector are stored in contiguous locations. Just like arrays, vector elements also can be traversed and accessed using iterators.

- What is the difference between `std::list` and `std::vector`
  https://www.softwaretestinghelp.com/lists-in-stl/
  the answer: Lists are sequential containers. Lists contain elements in non-contiguous locations.
  In case of the array and vector containers, as these containers store data in contiguous memory, insert operation in the middle of these containers proves to be very costly as we have to shift the existing elements accordingly to make space for the new element.
  The list is a container that overcomes this drawback of the array and vector containers. It allows us to insert elements anywhere in the list without causing much of an overhead. But lists are slower than vectors as far as traversal is concerned.
  A majority of list operations are similar to those of vectors.

## Task 2

- Run the Stack and Queue examples in the following link
  https://www.softwaretestinghelp.com/stacks-and-queues-in-stl/

> make sure you correct the syntax e.g `&lt;int&gt; becomes  <int>`

## Task 3

- Discuss the different types of iterators present in C++. You can refer to the following link
  https://www.geeksforgeeks.org/introduction-iterators-c/
  the answer: Based upon the functionality of the iterators, they can be classified into five major categories:

Input Iterators: They are the weakest of all the iterators and have very limited functionality. They can only be used in a single-pass algorithms, i.e., those algorithms which process the container sequentially, such that no element is accessed more than once.
Output Iterators: Just like input iterators, they are also very limited in their functionality and can only be used in single-pass algorithm, but not for accessing elements, but for being assigned elements.
Forward Iterator: They are higher in the hierarchy than input and output iterators, and contain all the features present in these two iterators. But, as the name suggests, they also can only move in a forward direction and that too one step at a time.
Bidirectional Iterators: They have all the features of forward iterators along with the fact that they overcome the drawback of forward iterators, as they can move in both the directions, that is why their name is bidirectional.
Random-Access Iterators: They are the most powerful iterators. They are not limited to moving sequentially, as their name suggests, they can randomly access any element inside the container. They are the ones whose functionality are same as pointers.

- What are the Benefits of Iterators
  the answer:
  1.Convenience in programming: It is better to use iterators to iterate through the contents of containers as if we will not use an iterator and access elements using [ ] operator, then we need to be always worried about the size of the container, whereas with iterators we can simply use member function end() and iterate through the contents without having to keep anything in mind.
  2.Code reusability: Now consider if we make v a list in place of vector in the above program and if we were not using iterators to access the elements and only using [ ] operator, then in that case this way of accessing was of no use for list (as they don’t support random-access iterators). However, if we were using iterators for vectors to access the elements, then just changing the vector to list in the declaration of the iterator would have served the purpose, without doing anything else So, iterators support reusability of code, as they can be used to access elements of any container.
  3.Dynamic processing of the container: Iterators provide us the ability to dynamically add or remove elements from the container as and when we want with ease.

## Links

- https://cpp.sh/
