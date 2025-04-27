# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        ll n,k;
        cin>>n>>k;
        vector<ll>arr;
        for(int i=0;i<n;++i){
            ll x;
            cin>>x;
            arr.ep(x);
        }
        sort(arr.begin(), arr.end());
        for(int i=1;i<n;++i){
            arr[i]+=arr[i-1];
        }
        if(binary_search(arr.begin(),arr.end(), k)==true)
            cout<<lower_bound(arr.begin(), arr.end(), k)-arr.begin()+1;
        else cout<<lower_bound(arr.begin(), arr.end(), k)-arr.begin();
    }

# Sol_tull
