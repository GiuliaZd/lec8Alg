# Activities

## Task 1

- What are the advantages of the C++ Standard Template Library (STL):
  the answer:

Reusability: One of the key advantages of the STL is that it provides a way to write generic, reusable code that can be applied to different data types. This can lead to more efficient and maintainable code.
Efficient algorithms: Many of the algorithms and data structures in the STL are implemented using optimized algorithms, which can result in faster execution times compared to custom code.
Improved code readability: The STL provides a consistent and well-documented way of working with data, which can make your code easier to understand and maintain.
Large community of users: The STL is widely used, which means that there is a large community of developers who can provide support and resources, such as tutorials and forums.

- What are the disadvantages of STL?
  the answer:Learning curve: The STL can be difficult to learn, especially for beginners, due to its complex syntax and use of advanced features like iterators and function objects.
  Lack of control: When using the STL, you have to rely on the implementation provided by the library, which can limit your control over certain aspects of your code.
  Performance: In some cases, using the STL can result in slower execution times compared to custom code, especially when dealing with small amounts of data.
- What are the main components of STL?
  the answer:
  Containers: The STL provides a range of containers, such as vector, list, map, set, and stack, which can be used to store and manipulate data.
  Algorithms: The STL provides a range of algorithms, such as sort, find, and binary_search, which can be used to manipulate data stored in containers.
  Iterators: Iterators are objects that provide a way to traverse the elements of a container. The STL provides a range of iterators, such as forward_iterator, bidirectional_iterator, and random_access_iterator, that can be used with different types of containers.
  Function Objects: Function objects, also known as functors, are objects that can be used as function arguments to algorithms. They provide a way to pass a function to an algorithm, allowing you to customize its behavior.
  Adapters: Adapters are components that modify the behavior of other components in the STL. For example, the reverse_iterator adapter can be used to reverse the order of elements in a container.

> You can refer to the following link: https://www.geeksforgeeks.org/the-c-standard-template-library-stl/

## Task 2

- Refer to `./src/non-manipulative.cpp`
  - Discuss how the program works
  - What are the Non-Manipulating Algorithms used in the program?
    the answer:
    Non-Manipulating Algorithms used in the program are:

sort(first_iterator, last_iterator) – To sort the given vector.
sort(first_iterator, last_iterator, greater<int>()) – To sort the given container/vector in descending order
reverse(first_iterator, last_iterator) – To reverse a vector. ( if ascending -> descending OR if descending -> ascending)
*max_element (first_iterator, last_iterator) – To find the maximum element of a vector.
*min_element (first_iterator, last_iterator) – To find the minimum element of a vector.
accumulate(first_iterator, last_iterator, initial value of sum) – Does the summation of vector elements

- Refer to `./src/manipulative.cpp`
  - Discuss how the program works
  - What are the Manipulating Algorithms used in the program?
    the answer:
    Manipulating used in the program are:

arr.erase(position to be deleted) – This erases selected element in vector and shifts and resizes the vector elements accordingly.
arr.erase(unique(arr.begin(),arr.end()),arr.end()) – This erases the duplicate occurrences in sorted vector in a single line.

> You can refer to the following link: https://www.geeksforgeeks.org/c-magicians-stl-algorithms/

## Task 3

- Refer to the following article. Reflect on the difference between Big Oh and little oh
  https://www.baeldung.com/cs/big-o-vs-little-o-notation
  the answer: Big-O and little-o notations have very similar definitions, and their difference lies in how strict they are regarding the upper bound they represent.
  the difference is that big-O may be asymptotically tight while little-o makes sure that the upper bound isn’t asymptotically tight.
  So O(g(n)) is a set of functions that are, after n_0, smaller than or equal to g(n). The function’s behavior before n_0 is unimportant since big-O notation (also little-o notation) analyzes the function for huge numbers.
  Little-o notation is used to denote an upper-bound that is not asymptotically tight. It is formally defined as:

o(g(n)) = \{f(n): for any positive constant c, there exists positive constant n_0 such that 0 \le f(n) < cg(n) for all n \ge n_0\}.

In this definition, the set of functions f(n) are strictly smaller than cg(n), meaning that little-o notation is a stronger upper bound than big-O notation. In other words, the little-o notation does not allow the function f(n) to have the same growth rate as g(n).

## Task 4

Refer to one of the following articles. Reflect on the differences between Big Oh, Big Omega and Theta.

- https://jarednielsen.com/big-o-omega-theta/
- https://www.codeandgadgets.com/big-oh-big-omega-and-theta-definitions/
- https://www.geeksforgeeks.org/difference-between-big-oh-big-omega-and-big-theta/

the answer:
We can think of Big O, Big Omega, and Big Theta like conditional operators:

Big O is like <=, meaning the rate of growth of an algorithm is less than or equal to a specific value, e.g: f(x) <= O(n^2)
Big Omega is like >=, meaning the rate of growth is greater than or equal to a specified value, e.g: f(x) >= Ω(n).
Big Theta is like ==, meaning the rate of growth is equal to a specified value, e.g: f(x) = Θ(n^2).
