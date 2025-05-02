# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        ll n;
        cin>>n;
        vector<bool>visit(10001,0);
        for(int i=0;i<n;++i){
            ll x;
            cin>>x;
            if(!visit[x])
                cout<<x<<' ';
            visit[x]=1;
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
          int n,t;
          cin>>n;
          while (n--)
          {
                cin>>t;
                if(++a[t]<=1)cout<<t<<' ';
          }
          
          return 0;
    }
