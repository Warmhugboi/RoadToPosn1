# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        string s;
        cin>>s;
        reverse(s.begin(), s.end());
        cout<<stoi(s);
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
          bool p=false;
          string k;
          cin>>k;
          reverse(all(k));
          for(auto&e:k){
                if(e>='1' and e<='9'){
                      p=true;
                }
                if(p)
                cout<<e;
          }
          return 0;
    }
