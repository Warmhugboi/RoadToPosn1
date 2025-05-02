# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        string s;
        cin>>s;
        int sum=0;
        for(auto&i:s){
            if(i>='a' && i<='z'){
                if(i=='a' or i=='e' or i=='i' or i=='o' or i=='u')
                    sum++;
            }
            else
                if(i=='A' or i=='E' or i=='I' or i=='O' or i=='U')
                    sum++;
        }
        cout<<sum;
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
    #define ck(a) for(auto&e:a)cout<<e<<' ';cout<<bp;
    int a[100005];
    signed main()
    {
          cin.tie(nullptr)->sync_with_stdio(false);
          string k;
          cin>>k;
          int s=0;
          for (auto&e:k)
          {
                char t=tolower(e);
                if(t=='a' or t=='e' or t=='i' or t=='o' or t=='u')++s;
          }
          cout<<s;
          return 0;
    }
