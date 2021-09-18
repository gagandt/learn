# BSP Tree
`incomplete`

BSP trees stand for Binary Space Partitioning Trees.
Apart from standard map and set operations, BSP trees also generally make certain other operations more efficient. Examples are range queries (Give me all points within this area) and nearest neighbor queries (What point is the closest to the one I provide).

These trees are conceptually similar to binary search trees. Instead of searching through the entire space, we divide the space into chunks. BSP’s do this by slicing the space using a plane. As an example, imagine we have a 100 x 100 x 100 cube full of points and are searching for the specific point (10, 20, 30). One can divide the cube into two sections: One where x is greater than 50 and one where it is less. Because we are looking for a point where x is equal to 10, we can immediately throw away the second half of the cube. BSP Trees recursively subdivide the structure into regions. The following is a great visualization of this:


### What are the sub-types?
1. K-D Trees
2. K-D-B Trees
3. hB Trees
4. BKD Trees


#### References
1. https://medium.com/@nickgerleman/the-bkd-tree-da19cf9493fb