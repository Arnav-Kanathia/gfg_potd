class Solution {
public:
    bool subArrayExists(int arr[], int n) {
        int sum = 0;
        unordered_set<int> s;
        s.insert(0);
        
        for (int i = 0; i < n; i++) {
            sum += arr[i];
            if (s.find(sum) != s.end())
                return true;
            s.insert(sum);
        }
        
        return false;
    }
};
