# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        ll n;
        cin>>n;
        vector<bool>visit(10001,0);
        for(int i=0;i<n;++i){
            ll x;
            cin>>x;
            if(!visit[x])
                cout<<x<<' ';
            visit[x]=1;
        }
    }

# Sol_tull
