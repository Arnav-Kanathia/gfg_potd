class Solution {
public:
    vector<int> repeatedRows(vector<vector<int>> &matrix, int M, int N) 
    { 
        unordered_map<string, int> mp;
        vector<int> out;

        for (int i = 0; i < matrix.size(); i++) {
            string str;
            for (int j = 0; j < matrix[0].size(); j++)
                str.push_back(matrix[i][j] ? '1' : '0');

            if (mp.find(str) != mp.end()) 
                out.push_back(i);
            else
                mp[str] = i;
        }

        return out;
    } 
};
