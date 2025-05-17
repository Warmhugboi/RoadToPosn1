# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    #define ep emplace_back




    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        int n,m,s,t;
        cin>>n>>m>>s>>t;
        vector<vector<pair<int,int>>>arr(n+1);
        vector<int>dist(n+1,INT_MAX);
        dist[s]=0;
        priority_queue<pair<int,int>, vector<pair<int,int>>, greater<pair<int,int>>>pq;
        for(int i=0;i<m;++i){
            int u,v,w;
            cin>>u>>v>>w;
            arr[u].ep(v,w);
            arr[v].ep(u,w);
        }
        pq.emplace(0,s);
        while(!pq.empty()){
            int u=pq.top().second, d=pq.top().first;
            pq.pop();
            if(d > dist[u]){
                continue;
            }
            for(auto&i:arr[u]){
                int v=i.first, w=i.second;
                if(dist[u]+w < dist[v]){
                    dist[v] = dist[u]+w;
                    pq.emplace(dist[v], v);
                }
            }
        }
        cout<<dist[t];




    }


# Sol_tull
    #include <iostream>
    #include <vector>
    #include <queue>
    #include <stack>
    #include <algorithm>
    #include <string.h>
    #include <math.h>
    #include <map>
    #include <tuple>
    #include <set>
    #include <unordered_map>
    #include <unordered_set>
    using namespace std;
    typedef int ll;
    int n, q, u, io;
    int INF = INT_MAX;
    #define all(x) x.begin(), x.end()
    void dijkstra(vector<vector<pair<ll,ll>>>& graph, int source, vector<ll>& dist)
    {
        dist.assign(n+3, INF); // Adjusted the size of dist vector
        //prev.assign(n+3, -1);   Initialize previous nodes
        priority_queue<pair<ll, ll>, vector<pair<ll, ll>>, greater<pair<ll, ll>>> pq;
    
        dist[source] = 0;
        pq.push({0, source});
    
        while (!pq.empty()) {
            ll u = pq.top().second;
            pq.pop();
            for (pair<ll,ll>& edge : graph[u]) {
                ll v = edge.first;
                ll weight = edge.second;
                // Update the distance and previous node if a shorter path is found
                if (dist[v] > dist[u] + weight) {
                    dist[v] = dist[u] + weight;
                    //prev[v] = u;  Store the previous node
                    pq.push({dist[v], v});
                }
            }
        }
    }
    
    int main()
    {
        cin.tie(NULL)->sync_with_stdio(false);
        vector<ll> dist,prev; // Vector to store the previous nodes
        cin >> n >> q >> u >> io;
        vector<vector<pair<ll,ll>>> a(n+20); // adjacency list
        for (int i = 0; i < q; ++i)
        {
            ll f,s,d;
            cin >> s >> d >> f;
            a[s].emplace_back(d,f);
            a[d].emplace_back(s,f);
        }
        dijkstra(a, u, dist);
    
        // Output shortest distances and paths taken
        cout<<dist[io]<<'\n';
        return 0;
    }
