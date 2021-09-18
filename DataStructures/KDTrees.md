# k-D Trees
`incomplete`
> k-d trees are a variant of BSP Trees which allow keys to include an arbitrary number of dimensions.

k-d Trees are one of the most common type of BSP Tree.
A k-d tree is implemented using a binary tree in a similar manner to a BST. The key difference is that the key comparison cycles through different dimensions at every level of the tree.

Like a Binary Search Tree, if a k-d tree is balanced, we are guaranteed a time complexity of O(log n) since every node divides the set in half. The key caveat is that this is only guaranteed when the tree is balanced.

### Advantages?
They are excellent for cases in which the data is static. An example could be an asset in a game.

### Disadvantages?
Standard k-d Trees don’t function particularly well when being dynamically updated.