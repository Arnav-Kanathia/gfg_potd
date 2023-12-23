class Solution
{
    public:
    int countOccurence(int arr[], int n, int k) {
        map<int,int> mp;
        int minCnt = n/k;
        for(int i = 0 ; i < n; ++i)
            ++mp[arr[i]];
        
        int out = 0;
        for(auto i: mp)
            if(i.second > minCnt)
                ++out;
                
        return out;
    }
};
