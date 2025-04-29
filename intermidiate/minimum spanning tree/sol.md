# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    #define ep emplace_back


    vector<int>p, rnk;

    int root(int u){
        if(p[u]==u) return u;
        return p[u]=root(p[u]);
    }

    bool iss(int u, int v){
        return root(u)==root(v);
    }

    void mrg(int u, int v){
        u=root(u);
        v=root(v);
        if(rnk[u]>rnk[v])
            p[v]=u;
        else{
            p[u]=v;
            if(rnk[u]==rnk[v]) ++rnk[v];
        }

    }

    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        int n,m;
        cin>>n>>m;
        vector<pair<int,pair<int,int>>>arr;
        p.resize(n+1);
        for(int i=1;i<=n;++i) p[i]=i;
        rnk.resize(n+1);
        for(int i=0;i<m;++i){
            int u,v,w;
            cin>>u>>v>>w;
            arr.ep(w,make_pair(u,v));
        }
        sort(arr.begin(), arr.end());
        int sum=0;
        for(auto&i:arr){
            int u=i.second.first, v=i.second.second, w=i.first;
            if(!iss(u,v)){
                mrg(u,v);
                sum+=w;
            }
        }
        cout<<sum;


    }


# Sol_tull
