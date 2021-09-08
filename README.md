# assignment2-kolluru

# Anurag Kolluru

### Chicago

Chicago is one of the beautiful citie's in USA. I've been there recently, just a few days back when i was comming to Maryville. it has many tourist's spots located in it, especially **Riverwalk** and **Skydeck**. Chicago's downtown is the best downtown that i have ever came accross in my life and it is worthy to spend a handsome of money on such trips.

***

# Navigation From Maryville To Tampa

1. First you have to go through St Louis, because it is the shortest possible route .
2. Then from Mt veron, Marion,Metropolis and Clarksville you'll reach Nashville
3. From there you must pass Chattanooga,Georgia,Lake City,Gainesville and Ocala to reach Tampa
4. Atlast you have to drive on the road between San antino and Spring lake
5. Finally you'll reach Tampa 
    1. Which is in between St.Petersburg,clearwater and lakeland
    2. These all are located in Florida state

# Items That I Carry To My Favourite Place

* Camera
* Short's and Tee's
* Shades
* Camping Kit
* Sunscreen

---

**[About Me](AboutMe.md)**

---

# Best Places To Hangout In Chicago

There are many Option's in Chicago but the below listed options are the finest of all, atleat from my perspective

| Item  | Location  | Price  |      
|---|---|---|
| Mc Salsa Chicken Burger  | MC Donalds  | 2.3$  |      
| 1/2 Chicken Peri Peri  | Nandos  | 16.3$  |      
| Taro Bubble tea  | Boba Blend  | 6.7$  |      
| 8pcs Chicken Family Meal  | Popoyes  | 22.3$  |

***

# Pithy Quotes

>Nobody reaches anywhere by believing.
― *Osho*

>Money is a tool, so I don't have to be.
― *Eddie Mumford*

---

# Topological Sorting Algorithm

>In computer science, a topological sort or topological ordering of a directed graph is a linear ordering of its vertices such that for every directed edge uv from vertex u to vertex v, u comes before v in the ordering. For instance, the vertices of the graph may represent tasks to be performed, and the edges may represent constraints that one task must be performed before another; in this application, a topological ordering is just a valid sequence for the tasks. Precisely, a topological sort is a graph traversal in which each node v is visited only after all its dependencies are visited. A topological ordering is possible if and only if the graph has no directed cycles, that is, if it is a directed acyclic graph (DAG). Any DAG has at least one topological ordering, and algorithms are known for constructing a topological ordering of any DAG in linear time. Topological sorting has many applications especially in ranking problems such as feedback arc set. Topological sorting is possible even when the DAG has disconnected components.

Source link: <https://en.wikipedia.org/wiki/Topological_sorting>


```
int n; // number of vertices
vector<vector<int>> adj; // adjacency list of graph
vector<bool> visited;
vector<int> ans;

void dfs(int v) {
    visited[v] = true;
    for (int u : adj[v]) {
        if (!visited[u])
            dfs(u);
    }
    ans.push_back(v);
}

void topological_sort() {
    visited.assign(n, false);
    ans.clear();
    for (int i = 0; i < n; ++i) {
        if (!visited[i])
            dfs(i);
    }
    reverse(ans.begin(), ans.end());
}

```

Source link: <https://cp-algorithms.com/graph/topological-sort.html>
