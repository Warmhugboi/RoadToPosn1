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
