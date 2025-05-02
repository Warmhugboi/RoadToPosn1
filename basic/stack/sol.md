# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        stack<ll>st;
        int n;
        cin>>n;
        for(int i=0;i<n;++i){
            string x;
            cin>>x;
            if(x=="push"){
                int y;
                cin>>y;
                st.emplace(y);
            }
            else if(x=="pop" && !st.empty()){
                cout<<st.top()<<'\n';
                st.pop();
            }
            else cout<<"null\n";
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
    #define ck(a) for(auto&e:a)cout<<e<<' ';cout<<bp;
    int a[100005];
    signed main()
    {
          cin.tie(nullptr)->sync_with_stdio(false);
          int n,k,s=0;
          cin>>n;
          string j;
          stack<int> t;
          while (n--)
          {
                cin>>j;
                if(j=="push"){
                      cin>>k;
                      t.emplace(k);
                }else{
                      if(t.empty())cout<<"null\n";
                      else{cout<<t.top()<<bp;t.pop();}
                }
          }
          
          return 0;
    }
