# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    #define ep emplace_back
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        
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
    const int mxn = 1e6 + 5;
    vector<int> a(mxn), v(mxn);
    signed main()
    {
          cin.tie(nullptr)->sync_with_stdio(false);
          int n, t;
          cin >> n;
          vector<int> d(n);
    
          for (int i = 0; i < n; ++i)
          {
                cin >> t;
                ++a[t];
                d[i] = t;
          }
          int tar = *max_element(all(a));
          // cout<<tar<<bp;
    
          for (int i = 0; i < n; ++i)
          {
                if (a[d[i]] == tar and !v[d[i]])
                {
                      cout << d[i] << ' ';
                      v[d[i]] = 1;
                }
          }
          cout << bp << tar;
          return 0;
    }
