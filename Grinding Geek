class Solution {
public:
    int solve(int i, int total, vector<int>& cost, vector<vector<int>>& dp){
        if(i == cost.size())
            return 0;

        if(dp[i][total] != -1)
            return dp[i][total];

        int t = 0, nt = 0;
        if(total >= cost[i]){   // for taking case
            int ac = cost[i] - floor(0.9 * cost[i]);    // actual cost that the user bears
            t = 1 + solve(i + 1, total - ac, cost, dp);
        }
        nt = solve(i + 1, total, cost, dp);	// for non taking case

        return dp[i][total] = max(t, nt);
    }

    int max_courses(int n, int total, vector<int>& cost) {
        vector<vector<int>> dp(n, vector<int>(total + 1, -1));
        return solve(0, total, cost, dp);
    }
};
