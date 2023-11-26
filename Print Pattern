class Solution {
public:
    vector<int> pattern(int N) {
        if (N <= 0)
            return {N};
            
        int toggle = -5;
        int c = N;
        vector<int> out;
        
        do {
            out.push_back(c);
            c += toggle;
            if (c <= 0)
                toggle = -toggle;
        } while (c != N);
        
        out.push_back(N);
        return out;
    }
};
