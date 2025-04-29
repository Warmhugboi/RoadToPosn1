# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    #define ep emplace_back

    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        int n,m,r;
        cin>>n>>m>>r;
        vector<vector<int>>a(n), b(m);
        for(int i=0;i<n;++i){
            for(int j=0;j<m;++j){
                int x;
                cin>>x;
                a[i].ep(x);
            }
        }
        for(int i=0;i<m;++i){
            for(int j=0;j<r;++j){
                int x;
                cin>>x;
                b[i].ep(x);
            }
        }
        int sum=0;

        for(int i=0;i<n;++i){
            for(int j=0;j<r;++j){
                sum=0;
                for(int k=0;k<m;++k){
                    sum+=a[i][k]*b[k][j];
                }
                cout<<sum<<' ';
            }
            cout<<'\n';
        }
    }

# Sol_tull
