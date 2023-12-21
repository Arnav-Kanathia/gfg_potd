class Solution {
public:
    int minCandy(int N, vector<int> &ratings) {
        vector<int> left(N, 1), right(N, 1);
        
        for (int i = 1; i < N; ++i)
            if (ratings[i] > ratings[i - 1])
                left[i] += left[i - 1];

        for (int i = N - 2; i >= 0; i--)
            if (ratings[i] > ratings[i + 1])
                right[i] += right[i + 1];

        int sum = 0;
        for (int i = 0; i < N; i++)
            sum += max(left[i], right[i]);

        return sum;
    }
};
