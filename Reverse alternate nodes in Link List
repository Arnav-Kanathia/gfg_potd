class Solution
{
    public:
    void rearrange(struct Node *odd)
    {
        struct Node* even = odd;
        struct Node* revOdd = NULL;
        struct Node* itr = odd;
        while(itr){
            struct Node* nextItr = itr->next;
            if(nextItr){
                even->next = itr->next->next;
                if(even->next)
                even = even->next;
                nextItr->next = revOdd;
                revOdd = nextItr;
            }else
                break;
            itr = even;
        }
        even->next = revOdd;
    }
};
