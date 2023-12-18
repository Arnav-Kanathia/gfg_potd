class Solution {
public:
    int findMaxSum(int *arr, int n) {
        int lastPrev = 0;
        int prev = arr[0];
        int curr = 0;

        for (int i = 1; i < n; ++i) {
            curr = max(prev, arr[i] + lastPrev);
            lastPrev = prev;
            prev = curr;
        }

        return max(lastPrev, prev);
    }
};
