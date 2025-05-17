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
        const int MX=1e18;
        const int MN=-MX;
        #define F first 
        #define S second
        signed main(){
            cin.tie(nullptr)->sync_with_stdio(false);
            int n,t,q;
            cin>>n>>q;
            vector<int>a(n+1);
            a[0]=0;
            for(int i=1;i<=n;++i){
                cin>>t;
                a[i]=a[i-1]+t;
            }
            while (q--)
            {
                cin>>n>>t;
                cout<<a[t]-a[n-1]<<bp;
            }
            
            return 0;
        }   
