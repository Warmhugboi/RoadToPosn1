# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    #define ep emplace_back

    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        ll n;
        cin>>n;
        vector<ll>arr;
        for(int i=0;i<n;++i){
            ll x;
            cin>>x;
            arr.ep(x);
        }
        sort(arr.begin(),arr.end());
        for(auto&i:arr) cout<<i<<' ';
        cout<<'\n';
        for(int i=n-1;i>=0;--i)
            cout<<arr[i]<<' ';
    }

# Sol_tull
