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
    #include <sstream>
    #define int long long
    using namespace std;
    using pii=pair<int,int>;
    #define bp '\n'
    #define vp cout<<bp;
    #define ck(a) for(auto&e:a)cout<<e<<' ';cout<<'\n';
    #define inv(a) for(auto&e:a)cin>>e;
    #define all(a) a.begin(),a.end()
    const int MX=1e18;
    const int MN=-MX;
    #define F first 
    #define S second
    #define val(i,j) (i>=0 and i<n and j>=0 and j<m)
    vector<pii> dir={{1,0},{-1,0},{0,1},{0,-1}};
    int n,m;
    
    signed main(){
        cin.tie(nullptr)->sync_with_stdio(false);
        int n,E,s,e,l,r,x,cnt=0;
        cin>>n>>E>>s>>e;
        vector<vector<pii>>a(n+1);
        vector<pii>d(n+1,{MX,-1});
        while(E--){
            cin>>l>>r>>x;
            a[l].emplace_back(r,x);
            a[r].emplace_back(l,x);
        }
        priority_queue<pii,vector<pii>,greater<pii>>pq;
        pq.emplace(0,s);
        d[s]={0,-1};
        while (!pq.empty())
        {
            auto [dist,src]=pq.top();
            pq.pop();
            for(auto&[v,w]:a[src]){
                if(d[v].F>d[src].F+w){
                    d[v].F=d[src].F+w;
                    d[v].S=src;
                    pq.emplace(d[v].F,v);
                }
            }
        }
        cout<<d[e].F<<bp;
        stringstream kl;
        stack<int>ss;
        while (e!=-1)
        {
            //kl<<e<<' ';
            ss.emplace(e);
            e=d[e].S;
            ++cnt;
        }
        while (!ss.empty())
        {
            cout<<ss.top()<<' ';
            ss.pop();
        }
        cout<<bp<<cnt-1;
        return 0;
    }   
