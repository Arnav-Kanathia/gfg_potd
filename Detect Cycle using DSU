class Solution {
public:
    vector<int> dsu;
    vector<bool> vis;
    vector<set<int>> g;

    int findDSU(int p) {
        if (dsu[p] < 0)
            return p;
        return dsu[p] = findDSU(dsu[p]);
    }

    void merge(int x, int y) {
        if (dsu[x] > dsu[y])
            swap(x, y);

        dsu[x] += dsu[y];
        dsu[y] = x;
    }

    bool dfs(int node, int par) {
        bool isCycle = false;
        vis[node] = true;

        for (auto child : g[node]) {
            if (child != par) {
                int x = findDSU(node);
                int y = findDSU(child);

                if (x == y)
                    return true;

                merge(x, y);
                isCycle = isCycle || dfs(child, node);
            }
        }

        return isCycle;
    }

    int detectCycle(int V, vector<int> adj[]) {
        dsu = vector<int>(V, -1);
        vis = vector<bool>(V, false);
        g = vector<set<int>>(V);

        for (int i = 0; i < V; i++) {
            for (auto x : adj[i])
                g[i].insert(x);
        }

        bool isCycle = false;

        for (int i = 0; i < V; i++) {
            if (!vis[i])
                isCycle = isCycle || dfs(i, -1);
        }

        return isCycle;
    }
};
