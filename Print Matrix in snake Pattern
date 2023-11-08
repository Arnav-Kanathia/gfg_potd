class Solution {
public:
    vector<int> snakePattern(vector<vector<int>> matrix) {
        bool toggle = false;
        vector<int> out;
        int n = matrix.size();

        for (int i = 0; i < n; ++i) {
            if (toggle) {
                for (int j = n - 1; j >= 0; --j) {
                    out.push_back(matrix[i][j]);
                }
            } else {
                for (int j = 0; j < n; ++j) {
                    out.push_back(matrix[i][j]);
                }
            }
            toggle = !toggle;
        }
        return out;
    }
};
