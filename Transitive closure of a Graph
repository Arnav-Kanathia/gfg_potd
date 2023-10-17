class Solution {
public:
    vector<vector<int>> transitiveClosure(int N, vector<vector<int>> graph)
    {
        vector<vector<int>> transitive(N, vector<int>(N, 0));

        for (int i=0; i<N; i++)
        {
            for (int j=0; j<N; j++)
            {
                transitive[i][j] = graph[i][j];
                if (i == j)
                {
                    transitive[i][j] = 1;
                }
            }
        }

        for (int k=0; k<N; k++)
        {
            for (int i=0; i<N; i++)
            {
                for (int j=0; j<N; j++)
                {
                    if (transitive[i][k] && transitive[k][j])
                    {
                        transitive[i][j] = 1;
                    }
                }
            }
        }

        return transitive;
    }
};
