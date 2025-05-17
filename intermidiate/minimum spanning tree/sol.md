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
    vector<int>par,rnk;
    vector<pair<int,pii>>edge;
    int n,l,E,r,x;
    int Find(int a){
        if(par[a]==a)return a;
        return par[a]=Find(par[a]);
    }
    bool Same(int a,int b){
        return Find(a)==Find(b);
    }
    void Union(int a,int b){
        a=Find(a);
        b=Find(b);
        if(rnk[a]>rnk[b]){
            par[b]=a;
        }
        else if(rnk[b]>rnk[a]){
            par[a]=b;
        }else{
            par[b]=a;
            ++rnk[a];
        }
    }
    signed main(){
        //freopen("input1.txt","r",stdin);
        cin.tie(NULL)->sync_with_stdio(false);
        cin>>n>>E;
        par.resize(n);
        rnk.resize(n);
        for(int i=0;i<n;++i){
            par[i]=i;
            rnk[i]=0;
        }
        while(E--){
            cin>>l>>r>>x;
            if(l>r)
                swap(l,r);
            edge.emplace_back(x,make_pair(l,r));
        }
        sort(all(edge));
        int s=0;
        for(auto&e:edge){
            int w=e.F,u=e.S.F,v=e.S.S;
            if(!Same(u,v)){
                Union(u,v);
                s+=w;
            }
        }
        cout<<s;
        return 0;
    }
