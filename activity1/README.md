# Activities

---

> [Course Feedback](https://ojp.metropolia.fi/lomakkeet/1/lomake.html?code=VFQwMEZFMzktMzAwMQ==)

---

## Task 1

- What is the difference between function overloading and function templates. You can refer to the programs in the `./src/` folder as well as [Links 2 and 3](#links) below.
  the answer:
  the difference between function overloading and function templates:
  Function overloading allows us to create multiple functions with the same name, so long as each identically named function has different parameter types (or the functions can be otherwise differentiated). How overloaded functions are differentiated: Number of parameters-Yes,Type of parameters -Yes(excludes typedefs, type aliases, and const qualifier on value parameters. Includes ellipses),
  Return type - No.
  Function templates: nstead of manually creating a bunch of mostly-identical functions or classes (one for each set of different types), we instead create a single template. Just like a normal definition, a template describes what a function or class looks like. Unlike a normal definition (where all types must be specified), in a template we can use one or more placeholder types. A placeholder type represents some type that is not known at the time the template is written, but that will be provided later.
  Once a template is defined, the compiler can use the template to generate as many overloaded functions (or classes) as needed, each using different actual types! The end result is the same -- we end up with a bunch of mostly-identical functions or classes (one for each set of different types). But we only have to create and maintain a single template, and the compiler does all the hard work for us.

- Rewrite the following program using templates

```cpp
#include <iostream>

int add(int x, int y)
{
    return x + y;
}

double add(double x, double y)
{
    return x + y;
}

int main()
{
    std::cout << add(1, 2); // calls add(int, int)
    std::cout << '\n';
    std::cout << add(1.2, 3.4); // calls add(double, double)

    return 0;
}
the answer:
#include <iostream>
template <typename T> // this is the template parameter declaration
T add (T x, T y) // this is the function template definition for add <T>
{
    return x + y;
}
int main()
{
    std::cout << add(1, 2); // calls add(int, int)
    std::cout << '\n';
    std::cout << add(1.2, 3.4); // calls add(double, double)

    return 0;
}

## Task 2

Refer to the following link:
https://www.softwaretestinghelp.com/vectors-in-stl/

Discuss the difference between

- Size() and capacity()
- begin() and cbegin()
- end() and cend()

the answer:
The difference between

- Size() and capacity(): size() returns the number of elements in the vector container.
Vector Capacity: various functions that act on vectors to determine their size, maximum size, etc.
- begin() and cbegin():begin(): Returns iterator pointed to the first element of the vector container. cbegin(): Returns a constant iterator pointing to the first element in the vector container.
- end() and cend(): end(): Returns an iterator pointing to the element that follows the last element in the vector. cend(): Returns a constant iterator pointing to the element following the last element of the vector container.

## Links

1. https://cpp.sh/
2. https://www.learncpp.com/cpp-tutorial/function-templates/
3. https://www.learncpp.com/cpp-tutorial/function-overload-differentiation/
4. https://www.geeksforgeeks.org/design-and-analysis-of-algorithms/
```
