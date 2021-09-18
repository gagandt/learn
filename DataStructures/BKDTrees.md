# BKD Tree

Bkd trees are a type of tree used for searching multidimensional data. This data can be anything from points in physical space to colors in a very large palette.

Compared to other trees in it’s class *(BSP Trees)*, Bkd trees are often faster and more space efficient than KDB trees and simpler than R-Trees.

### Ok, what trees before this?
1. github.com/gagandt/learn/blob/main/DataStructures/BSPTrees.md
2. github.com/gagandt/learn/blob/main/DataStructures/KDTrees.md

Bkd Trees manage to solve the space and insert efficiency problems. Bkd Trees are made up of multiple modified k-d Trees and unique methods for insertion.

### How does the structure looks like?
The tree combines a Binary Tree and B+ Tree. More specifically, the interior nodes must form a complete binary tree while the leaves are stored identically to those in a K-D-B tree.

### What's better in a BKD tree?
Because it is a complete binary tree, nodes do not need to store pointers to their children, instead multiplication may be used. Given a 1-indexed node at position i, the node's left child is always 2i and the right child it 2i + 1. Since the leaves also contain the points, nodes need not contain any value themselves. Smaller nodes mean more can be kept in cache. Adding to this is the large amount of points held in the leaves. This reduces the height of the tree.

An even bigger factor, and one of the most interesting parts about Bkd trees are that these internal trees are never modified. Bkd Trees use a clever scheme to add new points.

For insertions, Bkd Trees are more than two orders of magnitude faster than K-D-B Trees!

### Anything bad about it?
Tree construction and writing steps are very expensive.

#### References
1. https://medium.com/@nickgerleman/the-bkd-tree-da19cf9493fb