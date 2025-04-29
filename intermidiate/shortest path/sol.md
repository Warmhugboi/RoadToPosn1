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
