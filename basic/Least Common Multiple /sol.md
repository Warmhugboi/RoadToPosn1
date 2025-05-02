
# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        ll n,m;
        cin>>n>>m;
        cout<<(n*m)/__gcd(n,m);
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
          int a,b;
          cin>>a>>b;
          cout<<a/__gcd(a,b)*b;
          return 0;
    }
