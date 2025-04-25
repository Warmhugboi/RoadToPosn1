# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    
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
    // #include <bits/stdc++.h>
    using namespace std;
    /*
    #include <ext/pb_ds/assoc_container.hpp>
    #include <ext/pb_ds/tree_policy.hpp>
    using namespace __gnu_pbds;
    template <class T>
    using ordered_set = tree<T, null_type, less<T>, rb_tree_tag, tree_order_statistics_node_update>;
    template <class T>
    using ordered_multiset = tree<T, null_type, less_equal<T>, rb_tree_tag, tree_order_statistics_node_update>;
    */
    #define int long long
    #define ll long long
    using pil = pair<int, long long>;
    using pli = pair<long long, int>;
    using pll = pair<long long, long long>;
    using pii = pair<int, int>;
    using piii = pair<pair<int, int>, int>;
    using plll = pair<pair<ll, ll>, ll>;
    using pic = pair<int, char>;
    const int MX = 1000000000000000000LL; // 1e18
    const int MN = -MX;                   //-1e18
    const int MOD = 1e9 + 7;
    #define bp '\n'
    #define ull unsigned long long
    #define F first
    #define S second
    #define all(x) x.begin(), x.end()
    #define inv(a)          \
          for (auto &e : a) \
          {                 \
                cin >> e;   \
          }
    #define vp cout << '\n';
    #define inv2dm(a)             \
          for (auto &e : a)       \
                for (auto &c : e) \
                      cin >> c;
    #define ck(a)                 \
          for (auto &e : a)       \
                cout << e << ' '; \
          cout << '\n';
    #define ckpf(a)               \
          for (auto &e : a)       \
                printf("%d ", e); \
          printf("\n");
    #define ckpair(a)                                  \
          for (auto &[f, s] : a)                       \
                cout << "(" << f << ", " << s << ") "; \
          cout << '\n';
    #define LMX LLONG_MAX
    #define LMN LLONG_MIN
    #define ck2dm(a)                                                 \
          cout << '\n';                                              \
          for (auto &e : a)                                          \
          {                                                          \
                for (auto &c : e)                                    \
                      cout << ((c == MX or c == MN) ? 9 : c) << ' '; \
                cout << '\n';                                        \
          }
    #define ck2dmlr(a, l, r)                                                            \
          cout << '\n';                                                                 \
          for (int i = 0; i < l; ++i)                                                   \
          {                                                                             \
                for (int j = 0; j < r; ++j)                                             \
                {                                                                       \
                      cout << ((a[i][j] == MN or a[i][j] == MX) ? 9 : a[i][j]) << '\t'; \
                }                                                                       \
                cout << '\n';                                                           \
          }
    #define tostr(a) to_string(a)
    #define qs(a)                            \
          for (int i = 1; i < a.size(); ++i) \
                a[i] += a[i - 1];
    #define vpii vector<pair<int, int>>
    #define dir vector<pair<int, int>> direct = {{-1, 0}, {1, 0}, {0, 1}, {0, -1}};
    #define val(i, j) (i >= 0 and i < n and j >= 0 and j < m) ? 1 : 0
    #define vi vector<int>
    #define mt make_tuple
    #define mp make_pair
    #define db double
    signed main()
    {
          // freopen("input.txt","r",stdin);
          cin.tie(nullptr)->sync_with_stdio(false);
          int n,E,l,r,x,start,end;
          cin>>n>>E>>start>>end;
          vector<int> up(n+1,0),visit(n+1,false);
          vector<pii>d(n+1,{MX,-1});
          vector<vector<pii>>a(n+1);
          bool neg=false;
          while(E--){
                cin>>l>>r>>x;
                a[l].emplace_back(r,x);
          }
          queue<int>q;
          q.emplace(start);
          d[start].F=0;
          while (!q.empty())
          {
                int src=q.front();
                q.pop();
                for(auto&[v,w]:a[src]){
                      if(d[v].F>d[src].F+w){
                            d[v].F=d[src].F+w;
                            d[v].S=src;
                            if(++visit[v]==n){
                                  neg=true;
                                  goto jk;
                            }
                            q.emplace(v);
                      }
                }
          }
          jk:;
          if(neg){
                cout<<-1;
          }else{
                cout<<d[end].F<<bp;
                int k=d[end].S;
                vector<int>ans={end};
                do{
                      //cout<<k<<' ';
                      ans.emplace_back(k);
                      k=d[k].S;
    
                }while (k!=-1);
                reverse(all(ans));
                cout<<start;
                for(int i=1;i<ans.size();++i){
                      if(ans[i]>ans[i-1]){
                            cout<<'R';
                      }else{
                            cout<<'L';
                      }
                }
                cout<<end;
          }
          return 0;
    }
