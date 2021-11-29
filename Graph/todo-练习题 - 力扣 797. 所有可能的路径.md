### 练习题 - 力扣 797. 所有可能的路径

```c++
class Solution {
public:
    vector<vector<int>> res;
    vector<int> path;
    vector<vector<int>> allPathsSourceTarget(vector<vector<int>>& graph) {
        traverse(graph, 0, path);
        return res;
    }

    void traverse(vector<vector<int>>& graph, int s, vector<int>& path) {
        path.push_back(s);
        int n = graph.size(); // 长度等有几个点.
        if (s == n-1) { // 到达终点
            res.push_back(path);
            path.pop_back();
            return;
        }
        for (auto& v : graph[s]) {
            traverse(graph, v, path);
        }
        path.pop_back();
    }
};

```

