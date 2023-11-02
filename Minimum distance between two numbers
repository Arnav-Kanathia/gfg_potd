class Solution {
public:
    int minDist(int a[], int n, int x, int y) {
        int lastX, lastY, out;
        lastX = lastY = -1;
        out = INT_MAX;
        
        for(int i = 0; i < n; ++i) {
            if(a[i] == x)
                lastX = i;
            if(a[i] == y)
                lastY = i;
            
            if(lastX != -1 && lastY != -1)
                out = min(out, abs(lastX - lastY));
        }
        return out == INT_MAX ? -1 : out;
    }
};
