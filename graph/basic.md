# Basic

### DFS

#### Recursive

```cpp
unordered_map<int, bool> visited;  // Avoid loop
void traverse(Graph graph, int v)
{
    if (visited[v]) return;
    for (int neighbor: graph[v]) traverse(graph, neighbor);
}
```

#### Iterative

```cpp
void traverse(Graph graph, int root)
{
    stack<int> frontier;
    unordered_map<int, bool> visited;
    frontier.push(root);
    
    while (frontier.size() > 0)
    {
        int node = frontier.pop();
        if (visited.count(node)) continue;
        visited.add(node);
        for (int neighbor: graph[node]) frontier.push(neighbor);
    }
}
```

### BFS

```cpp
void traverse(Graph graph, int root)
{
    queue<int> frontier;
    unordered_map<int, bool> visited;
    frontier.push(root);
    
    while (frontier.size() > 0)
    {
        int node = frontier.dequeue();
        if (visited.count(node)) continue;
        visited.add(node);
        for (int neighbor: graph[node]) frontier.enqueue(neighbor);
    }
}
```

