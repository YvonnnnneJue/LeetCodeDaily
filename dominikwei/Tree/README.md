# TREE:

主要框架:

```c++
// TreeNode* prev
void dfs(TreeNode* root) {
  if (!root) return;
	dfs(root->left)
  // root do something
  // if (prev) { // do something }  prev = root; 保存前一节点.
  dfs(root->right)
}

void bfs(TreeNode* root) {
  queue<int> q;
  q.push(root);
  // int depth = 0 // 求深度
  while(!q.empty()) {
    int size = q.size();
    while(size--) {
      TreeNode* top = q.front();
      q.pop();
      if (q->left) q.push(q->left);
      if (q->right) q.push(q->right);
      // top do something
    }
    // depth++
  }
}
```







1. BST 保留前节点:

#### [501. Find Mode in Binary Search Tree](https://leetcode-cn.com/problems/find-mode-in-binary-search-tree/)

[783. Minimum Distance Between BST Nodes](https://leetcode-cn.com/problems/minimum-distance-between-bst-nodes/)

#### [面试题 17.12. BiNode](https://leetcode-cn.com/problems/binode-lcci/)

#### [897. Increasing Order Search Tree](https://leetcode-cn.com/problems/increasing-order-search-tree/)

