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
        vector<pair<int,string>>dist(n+1,make_pair(INT_MAX,to_string(s)));
        dist[s].first=0;
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
            if(d > dist[u].first){
                continue;
            }
            for(auto&i:arr[u]){
                int v=i.first, w=i.second;
                if(dist[u].first+w < dist[v].first){
                    dist[v].first = dist[u].first+w;
                    dist[v].second = dist[u].second + " " + to_string(v);
                    pq.emplace(dist[v].first, v);
                }
            }
        }
        cout<<dist[t].first<<'\n'<<dist[t].second<<'\n';
        int sum=0;
        for(auto&i:dist[t].second) if(i==' ') sum++;
        cout<<sum;




    }


# Sol_tull
