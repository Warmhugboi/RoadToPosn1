# Sol_top

      #include <bits/stdc++.h>
      using namespace std;
      #define ll long long
      #define mp make_pair
      #define F first
      #define S second
      #define ep emplace_back
      #define pll pair<ll,ll>
      #define For(i,a) for(int i=0;i<a;++i)
      #define str string
      #define MOD int(1e6+3)
      #define MAXN int(1e6+5)

      bool visit[int(1e5+5)];
      ll ct[int(1e5+5)];

      int main() {
      cin.tie(NULL)->sync_with_stdio(false);
      int n;
      cin>>n;
      vector<int>arr;
      ll MA=INT_MIN;
      for(int i=0;i<n;++i){
            int x;
            cin>>x;
            arr.ep(x);
            ct[x]+=1;
            MA=max(ct[x],MA);
      }
      for(int i=0;i<n;++i){
            if(!visit[arr[i]] && ct[arr[i]]==MA){
                  cout<<arr[i]<<' ';
            }
            visit[arr[i]]=1;
      }
      cout<<'\n'<<MA;

      }

# Sol_tull
      #include <bits/stdc++.h>
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
      const int mxn=1e6+5;
      vector<int>a(mxn),v(mxn);
      signed main()
      {
            cin.tie(nullptr)->sync_with_stdio(false);
            int n,t;
            cin>>n;
            vector<int>d(n);
            for (int i = 0; i < n; ++i)
            {
                  cin>>t;
                  ++a[t];
                  d[i]=t;
            }
            int tar=*max_element(all(a));
            for (int i = 0; i < n; ++i)
            {
                  if (a[d[i]] == tar and !v[d[i]])
                  {
                        cout << d[i] << ' ';
                        v[d[i]] = 1;
                  }
            }
            cout<<bp<<tar;
            return 0;
      }
