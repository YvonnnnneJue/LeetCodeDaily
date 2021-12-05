#### [5944. Step-By-Step Directions From a Binary Tree Node to Another](https://leetcode-cn.com/problems/step-by-step-directions-from-a-binary-tree-node-to-another/)

复习: DFS打印所有二叉树路径

#### [257. Binary Tree Paths](https://leetcode-cn.com/problems/binary-tree-paths/)

```c++
/**
 * Definition for a binary tree node.
 * struct TreeNode {
 *     int val;
 *     TreeNode *left;
 *     TreeNode *right;
 *     TreeNode() : val(0), left(nullptr), right(nullptr) {}
 *     TreeNode(int x) : val(x), left(nullptr), right(nullptr) {}
 *     TreeNode(int x, TreeNode *left, TreeNode *right) : val(x), left(left), right(right) {}
 * };
 */
class Solution {
public:
    string path, p1, p2;
    string getDirections(TreeNode* root, int startValue, int destValue) {
        if(root == nullptr) return "";
        transval(root, startValue, destValue);
        int i = 0, j = 0;
        cout << p1 << " " << p2 << endl;
        while(p1[i] == p2[j]) i++, j++;
        return string(p1.size() - i, 'U') + p2.substr(j);
    }
    void transval(TreeNode* root, int s, int d) {
            if (root->val == s) p1 = path;
            if(root->val == d) p2 = path;
            if(root->left) path += 'L', transval(root->left, s, d), path.pop_back();
            if(root->right) path += 'R', transval(root->right, s, d), path.pop_back();
    }
};
```

