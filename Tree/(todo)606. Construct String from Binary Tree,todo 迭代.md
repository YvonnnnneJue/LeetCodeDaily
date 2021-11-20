#### [606. Construct String from Binary Tree](https://leetcode-cn.com/problems/construct-string-from-binary-tree/)

根据二叉树构建字符串

![image-20211120205020813](/Users/dominikwei/Library/Application Support/typora-user-images/image-20211120205020813.png)

![image-20211120205029875](/Users/dominikwei/Library/Application Support/typora-user-images/image-20211120205029875.png)

```c++
 // return 根节点 + "(" + 左子树节点 + ")" + "(" + 右子树节点 + ")", root(left)(right)
 // 特定条件:
 // 1. 如果左右节点都不存在, root 而不是 root()()
 // 2. 如果left为空节点,则输出root()(right)
 // 3. 如果右节点为空,则忽略右节点的(),输出root(left)
class Solution {
public:
    string tree2str(TreeNode* root) {
        string res = "";
        if (!root) return res;
        if (!root->left && !root->right) return to_string(root->val);// 如果左右节点都不存在
        if(!root->right){ // 如果右节点为空
            return to_string(root->val) + "(" + tree2str(root->left) + ")";
        }
      	// left为空 + 左右节点都存在的情况
        return to_string(root->val) + "(" + tree2str(root->left) + ")("+ tree2str(root->right) + ")";
    }
};
```

