#### [671. Second Minimum Node In a Binary Tree](https://leetcode-cn.com/problems/second-minimum-node-in-a-binary-tree/)

求二叉树中第二小的节点

```c++
class Solution {
public:
    // 看题意,他不是一个搜索二叉树
    // 求左右子节点中的最小值
    int findSecondMinimumValue(TreeNode* root) {
        return traversal(root, root->val);
    }
    /**
    * val 保留root值
    **/
    int traversal(TreeNode* root, int val) {
        if (!root) return -1;
        if (root->val > val) return root->val;
        // 寻找左右子节点中,第一个大于自己的节点.
        int l = traversal(root->left, val);
        int r = traversal(root->right, val);
        // 存在两个子节点
        if (l >= 0 && r >= 0) return min(l,r);
        // 存在0个子节点
        return max(l,r);
    }
};
```

