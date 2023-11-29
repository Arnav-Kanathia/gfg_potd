class Solution {
public:
    int isEulerCircuit(int v, vector<int> adj[]) {
        int even = 0, odd = 0;
        for (int i = 0; i < v; i++) {
            if (adj[i].size() & 1)
                ++odd;
            else
                ++even;
        }

        return even == v ? 2 : (odd > 0 && odd == 2);
    }
};
