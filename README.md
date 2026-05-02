 Key Features

*  Tree structure (Category → Subcategory → Product)
*  DFS search to find category
*  Only leaf nodes (products) considered
*  Score = 0.6 * popularity + 0.4 * rating
*  Sorted by highest score
*  Returns Top-N products


Solution

1. Build product tree
2. Find category using DFS
3. Collect all products under it
4. Calculate score
5. Sort المنتجات
6. Return top-N
