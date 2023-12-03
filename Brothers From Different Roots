class Solution {
public:
    void inorder(Node* root, vector<int>& v) {
        if (root == NULL)
            return;

        inorder(root->left, v);
        v.push_back(root->data);
        inorder(root->right, v);
    }

    int countPairs(Node* root1, Node* root2, int x) {
        vector<int> t1, t2;

        inorder(root1, t1);
        inorder(root2, t2);

        int i = 0, j = t2.size() - 1;
        int out = 0;

        while (i < t1.size() && j >= 0) {
            int sum = t1[i] + t2[j];
            if (sum > x)
                --j;
            else if (sum < x)
                ++i;
            else {
                ++out;
                ++i;
                --j;
            }
        }
        return out;
    }
};
