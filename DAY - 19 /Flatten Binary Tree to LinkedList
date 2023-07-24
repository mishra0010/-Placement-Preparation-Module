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

    TreeNode* helper(TreeNode* root){
        if(root==NULL){
            return NULL;
        }
        TreeNode* left = helper(root->left);
        TreeNode* right = helper(root->right);
        if(left == NULL && right == NULL){
            return root;
        }
        if(left == NULL){
            root->right = right;
            return root;
        }
        if(right == NULL){
            root->left = NULL;
            root->right = left;
            return root;
        }
        TreeNode* last = left;
        while(last->right!=NULL){
            last = last ->right;
        }
        root->right = left;
        last->right = right;
        root->left = NULL;
        return root;
    }

    void flatten(TreeNode* root) {
        root = helper(root);
    }
};
