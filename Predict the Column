class Solution {
public:
    int columnWithMaxZeros(vector<vector<int>> &arr, int n) {
        int maxZeros = 0;
        int columnIdx = -1;
        
        for (int j = 0; j < n; j++) {
            int zerosCount = 0;
            for (int i = 0; i < n; i++) {
                if (arr[i][j] == 0) {
                    zerosCount++;
                }
            }
            
            if (zerosCount > maxZeros) {
                maxZeros = zerosCount;
                columnIdx = j;
            }
        }
        
        return columnIdx;
    }
};
