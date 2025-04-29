# Sol_top

        #include <bits/stdc++.h>
        using namespace std;
        #define ll long long
        #define ep emplace_back
        
        int main(){
            cin.tie(NULL)->sync_with_stdio(false);
            int n,q;
            cin>>n>>q;
            vector<ll>arr{0};
            ll sum=0;
            for(int i=0;i<n;++i){
                int x;
                cin>>x;
                sum+=x;
                arr.ep(sum);
            }
            for(int i=0;i<q;++i){
                int l,r;
                cin>>l>>r;
                cout<<arr[r]-arr[l-1]<<'\n';
            }
         }

# Sol_tull
