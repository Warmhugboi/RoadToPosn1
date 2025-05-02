# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        ll n,sum=0;
        cin>>n;

        for(int i=0;i<n;++i){
            ll x;
            cin>>x;
            if(x%2==0)
                sum++;
        }
        cout<<sum<<' '<<n-sum;
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
    int ans[2];
    signed main()
    {
          cin.tie(nullptr)->sync_with_stdio(false);
          int n,t;
          cin>>n;
          while (n--)
          {
                cin>>t;
                ++ans[t%2==1];
          }
          cout<<ans[0]<<' '<<ans[1];
          return 0;
    }
