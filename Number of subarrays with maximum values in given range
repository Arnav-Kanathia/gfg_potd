class Solution{
public:
    long countSubarrays(int a[], int n, int L, int R)
    {
        long out = 0, range = 0;
        long i = 0;
        
        for (long j = 0; j < n; ++j)
        {
            if (a[j] >= L && a[j] <= R)
                range = j - i + 1;
            else if (a[j] > R)
                range = 0, i = j + 1;

            out += range;
        }
        
        return out;
    }
};
