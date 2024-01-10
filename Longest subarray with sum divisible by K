class Solution {
public:
    int longSubarrWthSumDivByK(int arr[], int n, int k) {
        unordered_map<int, int> mp;
        mp[0] = -1;
        
        int out = 0, sum = 0;
        
        for (int i = 0; i < n; i++) {
            sum += arr[i];
            int rem = sum % k;
            
            if (rem < 0)
                rem += k;
            
            if (mp.find(rem) != mp.end())
                out = max(out, i - mp[rem]);
            else
                mp[rem] = i;
        }
        
        return out;
    }
};
