DIAMETER OF BINARY TREE
https://leetcode.com/problems/diameter-of-binary-tree/description/

```cpp
class Solution {
    int ans = 0;

private:
int height(TreeNode* root) {
        if (!root) return 0;

        int lh = height(root->left);
        int rh = height(root->right);

        ans = max(ans, lh + rh);

        return 1 + max(lh, rh);
    }
public:
int diameterOfBinaryTree(TreeNode* root) {
        height(root);
        return ans;
    }
};
```
