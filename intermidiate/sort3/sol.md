# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    #define ep emplace_back

    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        int n;
        cin>>n;
        vector<ll>a, b;
        bool visit[n+1];
        for(auto&i:visit) i=0;
        for(int i=0;i<n;++i){
            ll x;
            cin>>x;
            if(x%2==0){
                a.ep(x);
                visit[i]=1;
            }
            else b.ep(x);
        }
        sort(a.begin(), a.end());
        sort(b.rbegin(), b.rend());
        int j=0,k=0;
        for(int i=0;i<n;++i){
            if(visit[i]==1){
                cout<<a[j]<<" ";
                ++j;
            }
            else {
                cout<<b[k]<<" ";
                ++k;
            }
        }
    }

# Sol_tull
