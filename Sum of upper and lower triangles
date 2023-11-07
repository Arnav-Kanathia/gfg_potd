class Solution {
public:
    vector<int> sumTriangles(const vector<vector<int> >& matrix, int n) {
        vector<int> out(2, 0);
        
        for (int i = 0; i < n; ++i) {
            for (int j = 0; j < n; ++j) {
                if (i <= j)
                    out[0] += matrix[i][j];
                if (i >= j)
                    out[1] += matrix[i][j];
            }
        }
        return out;
    }
};
