class Solution{
public:
    vector<string> winner(string arr[],int n)
    {
        unordered_map<string,int> mp;
        for(int i = 0; i < n ; ++i)
            ++mp[arr[i]];
        
        string out;
        int cnt = 0;
        for(auto i: mp){
            if(cnt < i.second){
                cnt = i.second;
                out = i.first;
            } else if(cnt == i.second){
                if(out > i.first)
                    out = i.first;
            }
        }
        return {out, to_string(cnt)};
    }
};
