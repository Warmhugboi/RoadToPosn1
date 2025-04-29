# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    #define ep emplace_back

    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        int n,q;
        cin>>n>>q;
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
        for(int i=0;i<q;++i){
            ll x;
            cin>>x;
            if(binary_search(arr.begin(), arr.end(), x)==1){
                cout<<lower_bound(arr.begin(), arr.end(), x)-arr.begin()+1<<'\n';
            }
            else cout<<lower_bound(arr.begin(), arr.end(), x)-arr.begin()<<'\n';
        }

    }

# Sol_tull
