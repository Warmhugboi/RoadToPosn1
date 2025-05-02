# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        ll n,t;
        cin>>n;
        ll MA=INT_MIN, MI=INT_MAX;
        for(int i=0;i<n;++i){
            ll x;
            cin>>x;
            MA=max(MA,x);
            MI=min(MI,x);
        }
        cin>>t;
        if(t==1) cout<<MA;
        else cout<<MI;
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
    // #include <bits/stdc++.h>
    using namespace std;
    #define int long long
    using pii = pair<int, int>;
    const int MX = 1000000000000000000LL; // 1e18
    const int MN = -MX;                   //-1e18
    const int MOD = 1e9 + 7;
    #define bp '\n'
    #define F first
    #define S second
    #define all(x) x.begin(), x.end()
    #define inv(a) for(auto &e : a){cin >> e;}
    #define vp cout << '\n';
    int a[100005];
    signed main()
    {
          cin.tie(nullptr)->sync_with_stdio(false);
          int n,mn=MX,mx=MN,t;
          cin>>n;
          while (n--)
          {
                cin>>t;
                mn=min(mn,t);
                mx=max(mx,t);
          }
          cin>>t;
          if(t==0){
                cout<<mn;
          }else{
                cout<<mx;
          }
          return 0;
    }
