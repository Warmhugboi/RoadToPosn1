# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    #define ep emplace_back

    int visit[105][105];
    int row[4]={1,0,-1,0};
    int col[4]={0,1,0,-1};

    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        int n,m;
        cin>>n>>m;
        vector<string>arr;
        queue<pair<int,pair<int,int>>>q;
        for(int i=0;i<n;++i){
            string x;
            cin>>x;
            arr.ep(x);
        }
        visit[0][0]=1;
        q.emplace(1,make_pair(0,0));
        while(!q.empty()){
            int w=q.front().first, x=q.front().second.first, y=q.front().second.second;
            q.pop();
            for(int i=0;i<4;++i){
                int xx=x+row[i], yy=y+col[i];
                if(xx<0 || yy<0 || xx>=n || yy>=m){
                    continue;
                }
                if(arr[xx][yy]=='X')
                    continue;
                if(visit[xx][yy]!=0)
                    continue;
                visit[xx][yy]=w+1;
                q.emplace(w+1,make_pair(xx,yy));
            }
        }
        cout<<visit[n-1][m-1];


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
        cin>>n>>m;
        vector<string>a(n);
        for(auto&e:a){
            cin>>e;
        }
        queue<array<int,3>>q;
        q.push({0,0,0});
        while (!q.empty())
        {
            auto[i,j,d]=q.front();
            q.pop();
            if(i==n-1 and j==m-1){
                cout<<d+1;
                return 0;
            }
            a[i][j]='X';
            for(auto&[f,s]:dir){
                int o=f+i,p=s+j;
                if(!val(o,p) or a[o][p]=='X')
                continue;
                q.push({o,p,d+1});
            }
        }
        return 0;
    }   
