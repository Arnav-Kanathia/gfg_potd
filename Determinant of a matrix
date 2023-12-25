class Solution {
public:
    int determinantOfMatrix(vector<vector<int>> mat, int n) {
        if (n == 1) {
            return mat[0][0];
        }
        if (n == 2) {
            return mat[0][0] * mat[1][1] - mat[0][1] * mat[1][0];
        }

        int sign = 1, ans = 0;
        vector<vector<int>> m(n - 1, vector<int>(n - 1));

        for (int row = 0; row < n; ++row) {
            int k = 0;
            for (int i = 0; i < n; ++i) {
                if (i != row) {
                    for (int j = 1; j < n; ++j)
                        m[k][j - 1] = mat[i][j];

                    k++;
                }
            }
            ans += sign * (mat[row][0]) * determinantOfMatrix(m, n - 1);
            sign *= -1;
        }
        return ans;
    }
};
