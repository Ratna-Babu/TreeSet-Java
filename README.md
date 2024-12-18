# TreeSet in Java

This is a simple demonstration of using the `TreeSet` class in Java. It shows how elements are added to the set, how `TreeSet` ensures sorted order, and how to access elements using an iterator.

## What is a TreeSet?

A `TreeSet` is a class that implements the `Set` interface in Java. It is part of the `java.util` package and provides a collection of unique elements that are automatically sorted in their natural order, or by a comparator provided at the time of creation.

### Key Features of TreeSet:
- **Sorted Order**: Elements in a `TreeSet` are sorted according to their natural ordering (for numbers, it's ascending order) or by a specified comparator.
- **No Duplicates**: Like all sets, a `TreeSet` does not allow duplicate elements.
- **Efficient Operations**: It provides efficient methods for element insertion, removal, and lookup with a time complexity of O(log n) for most operations.
- **Navigable**: Since `TreeSet` implements `NavigableSet`, you can perform operations like finding the closest elements to a given value.

## Code Explanation

In the provided Java code, we create a `TreeSet` object named `numbers` and perform the following operations:

1. **Creating the TreeSet**:
   - A new `TreeSet` is initialized. This `TreeSet` will automatically arrange the elements in ascending order.
   - The elements `2`, `3`, and `1` are added to the `TreeSet`.

2. **Printing the TreeSet**:
   - The contents of the `TreeSet` are printed. Since `TreeSet` sorts its elements, the output will show the elements in ascending order.

3. **Accessing Elements using Iterator**:
   - An `Iterator` is created to access each element in the `TreeSet`.
   - We loop through the elements using `hasNext()` to check if there are more elements and `next()` to retrieve the next element.
   - The elements are printed with commas in between.

### Code
```Java
import java.util.Set;
import java.util.TreeSet;
import java.util.Iterator;

public class TreeSetDemo {
    public static void main(String[] args) {
        Set<Integer> numbers = new TreeSet<>();
        numbers.add(2);
        numbers.add(3);
        numbers.add(1);
        System.out.println("Set using TreeSet: " + numbers);
        System.out.print("Accessing elements using iterator(): ");
        Iterator<Integer> iterate = numbers.iterator();
        while (iterate.hasNext()) {
            System.out.print(iterate.next());
            System.out.print(",");
        }
    }
}
```
### Output
```
Set using TreeSet: [1, 2, 3]
Accessing elements using iterator(): 1,2,3,
```

As shown in the output:
- The `TreeSet` automatically sorts the elements in ascending order, so when we print the set, it displays `[1, 2, 3]`.
- Using the iterator, we access and print each element one by one, separated by commas.

## Key Methods in TreeSet:

- **add(E e)**: Adds the specified element to the set if it is not already present.
- **iterator()**: Returns an iterator over the elements in the set.
- **contains(Object o)**: Checks if the set contains the specified element.
- **remove(Object o)**: Removes the specified element from the set.
- **size()**: Returns the number of elements in the set.
- **clear()**: Removes all elements from the set.
- **isEmpty()**: Checks if the set is empty.
- **first()**: Returns the first (lowest) element in the set.
- **last()**: Returns the last (highest) element in the set.

## Conclusion

The `TreeSet` class is useful when you need a collection of unique elements that are automatically sorted. It is efficient for operations like searching, adding, and removing elements, and it is often used when the order of elements matters.

Feel free to modify the code to experiment with different operations, such as adding more elements, removing items, or using a custom comparator for sorting!

