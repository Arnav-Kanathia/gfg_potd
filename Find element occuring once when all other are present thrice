class Solution {
  public:
    int singleElement(int arr[], int N) {
        vector<int> bits(32, 0);
        for (int i = 0; i < N; i++) {
            for (int j = 0; j < 32; j++) {
                bits[j] += arr[i] & 1;
                arr[i] >>= 1;
            }
        }

        int ans = 0;
        for (int i = 0; i < 32; i++)
            if (bits[i] % 3 != 0)
                ans += 1 << i;

        return ans;
    }
};
