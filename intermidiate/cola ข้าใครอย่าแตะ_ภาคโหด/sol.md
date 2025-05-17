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
    signed main(){
        cin.tie(nullptr)->sync_with_stdio(false);
        int n,t,l,r,q;
        cin>>n>>q;
        vector<int>a(n);
        inv(a)    
        sort(all(a));
        for(int i=1;i<n;++i){
            a[i]+=a[i-1];
        }
        while (q--)
        {
            cin>>t;
            auto p=upper_bound(all(a),t);
            cout<<p-a.begin()<<bp;
        }
        return 0;
    }   
