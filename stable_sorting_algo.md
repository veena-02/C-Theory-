[Stable VS Unstable Sorting Algorithms](https://javarevisited.blogspot.com/2017/06/difference-between-stable-and-unstable-algorithm.html#axzz74RbOKIMi)

Stability is mainly important when we have key value pairs with duplicate keys possible (like people names as keys and their details as values). And we wish to sort these objects by keys

A sorting algorithm is said to be stable if two objects with equal keys appear in the same order in sorted output as they appear in the input array to be sorted.

### stable algorithms are 
--- Merge Sort, Insertion Sort, Bubble Sort, and Binary Tree Sort.
### unstable algorithms are 
--- QuickSort, Heap Sort, and Selection sort 

### Do we care for simple arrays like array of integers?
When equal elements are indistinguishable, such as with integers, or more generally, any data where the entire element is the key, stability is not an issue. Stability is also not an issue if all keys are different.

![image](https://user-images.githubusercontent.com/59028294/130581669-58dc4ffd-ff3d-48e4-a74b-08e334472d2a.png)




