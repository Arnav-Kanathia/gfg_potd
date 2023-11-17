class Solution {
public:
    Node* head;
    Node* tail;

    void inorder(Node *root) {
        if (!root)
            return;

        inorder(root->left);
        
        Node* curr = new Node;
        curr->data = root->data;
        if (tail) {
            tail->right = curr;
            curr->left = tail;
        } else 
            head = curr;
        tail = curr;

        inorder(root->right);
    }

    Node *bTreeToCList(Node *root) {
        tail = head = NULL;

        inorder(root);

        head->left = tail;
        tail->right = head;

        return head;
    }
};
