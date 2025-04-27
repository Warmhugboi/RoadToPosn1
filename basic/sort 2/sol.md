# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    
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
        for(int i=0;i<n;++i)
            cout<<arr[i]<<' '<<arr[n-i-1]<<' ';
    }

# Sol_tull
