class Solution {
public:
    int getMinDiff(int arr[], int n, int k) {
        sort(arr, arr + n);
        int out = arr[n - 1] - arr[0];

        for (int i = 0; i < n - 1; ++i) {
            if (arr[i + 1] - k >= 0) {
                int nax = max(arr[i] + k, arr[n - 1] - k);
                int nin = min(arr[i + 1] - k, arr[0] + k);
                out = min(out, nax - nin);
            }
        }
        return out;
    }
};
