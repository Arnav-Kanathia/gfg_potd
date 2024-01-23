class Solution {
public:
    vector<int> findOrder(int n, int m, vector<vector<int>> pre) {
        vector<int> graph[n];
        vector<int> degree(n, 0);

        for (auto i : pre) {
            degree[i[0]]++;
            graph[i[1]].push_back(i[0]);
        }

        queue<int> q;
        for (int i = 0; i < n; ++i)
            if (!degree[i])
                q.push(i);

        vector<int> ans;
        while (!q.empty()) {
            int front = q.front();
            q.pop();

            ans.push_back(front);
            for (auto i : graph[front]) {
                degree[i]--;
                if (degree[i] == 0)
                    q.push(i);
            }
        }

        for (auto i : degree) {
            if (i >= 1)
                return {};
        }

        return ans;
    }
};
