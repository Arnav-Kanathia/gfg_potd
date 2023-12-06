class Solution {
public: 
    void cntX(int n, int& X, int& cnt){
        while(n){
            if(n % 10 == X)
                ++cnt;
            n /= 10;
        }
    }

    int countX(int L, int R, int X) {
        int cnt = 0;
        
        for(int i = L + 1; i < R; i++)
            cntX(i, X, cnt);

        return cnt;
    }
};
