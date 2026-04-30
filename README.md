
Program Description

The Product Recommendation Engine is a C++ application that uses a tree data structure to organize products in a hierarchical manner similar to real-world e-commerce platforms.

The tree consists of:
Root node → “All Products”
Category nodes → Electronics, Clothing, Books
Sub-category nodes → Phones, Laptops, Shoes, etc.
Leaf nodes (products) → Actual items like iPhone 16, MacBook Pro, etc.

Each product (leaf node) contains:

Popularity (user clicks / demand)
Rating (user reviews)
Price

Working Principle

When a user selects a category:

The system searches the category node using DFS (Depth First Search).
It collects all products (leaf nodes) under that category.
Each product is assigned a composite score based on:
60% Popularity
40% Rating
Products are sorted based on score.
The system returns the Top-N recommended products.

Core Data Structures Used
1. Tree Structure
Implemented using ProductNode
Each node contains:
Data (id, name, etc.)
Pointer to parent
List of children
2. Stack
Used in iterative DFS search
3. Vector
Stores children and product lists
4. Smart Pointers (shared_ptr)
Used for safe memory management

Proposed Solution

To efficiently implement a recommendation system:

Step 1: Build Hierarchical Tree
Create nodes for categories and products
Link them using parent-child relationship

Step 2: Search Category (DFS)
Use iterative DFS to find the required category
Time complexity: O(n)

Step 3: Collect Products
Use recursive traversal
Collect all leaf nodes (products) under that category

Step 4: Rank Products
Compute composite score
Sort using std::sort()
Time complexity: O(k log k)
Step 5: Return Top-N Results
Trim the sorted list to required size

Time & Space Complexity

| Operation      | Time Complexity | Space Complexity |
| -------------- | --------------- | ---------------- |
| DFS Search     | O(n)            | O(h)             |
| Collect Leaves | O(k)            | O(k)             |
| Sorting        | O(k log k)      | O(k)             |
| Tree Storage   | —               | O(n)             |

Where:

n= total nodes
k = products in category
h= height of tree



Advantages of This Approach

* Efficient hierarchical data handling
* Scalable for large product catalogs
* Real-time recommendation generation
* Easy to extend (add filters like price, brand, etc.)




