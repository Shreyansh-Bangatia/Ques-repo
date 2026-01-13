145. Binary Tree Postorder Traversal
Given the root of a binary tree, return the postorder traversal of its nodes' values.

class Solution {
public:
    vector<int> postorderTraversal(TreeNode* root) {
        if(root==NULL) return {};
       vector<int>ans;
       vector<int>Left = postorderTraversal(root->left);
       ans.insert(ans.end(),Left.begin(),Left.end());
       vector<int>Right = postorderTraversal(root->right);
         ans.insert(ans.end(),Right.begin(),Right.end());
         ans.push_back(root->val);
         return ans;



    }
};



94. Binary Tree Inorder Traversal
Given the root of a binary tree, return the inorder traversal of its nodes' values.


class Solution {
public:
    vector<int> inorderTraversal(TreeNode* root) {
        if (root == NULL) return {};

        vector<int> ans;

        vector<int> left = inorderTraversal(root->left);
        ans.insert(ans.end(), left.begin(), left.end());

        ans.push_back(root->val);

        vector<int> right = inorderTraversal(root->right);
        ans.insert(ans.end(), right.begin(), right.end());

        return ans;
    }
};




144. Binary Tree Preorder Traversal
Given the root of a binary tree, return the preorder traversal of its nodes' values.

class Solution {
public:
    vector<int> preorderTraversal(TreeNode* root) {
    if (root == NULL) return {};

    vector<int> ans;
    ans.push_back(root->val);  
    vector<int> left = preorderTraversal(root->left);
    vector<int> right = preorderTraversal(root->right);

    ans.insert(ans.end(), left.begin(), left.end());
    ans.insert(ans.end(), right.begin(), right.end());

    return ans;
}

}; 