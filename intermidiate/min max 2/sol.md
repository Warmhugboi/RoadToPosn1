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
      #define int long long
      using namespace std;
      using pii=pair<int,int>;
      #define bp '\n'
      #define vp cout<<bp;
      #define ck(a) for(auto&e:a)cout<<e<<' ';cout<<'\n';
      #define all(a) a.begin(),a.end()
      const int MX=1e18;
      const int MN=-MX;
      #define F first 
      #define S second
      vector<int>a(100005);
      signed main(){
          cin.tie(nullptr)->sync_with_stdio(false);
          int t,n;
          cin>>n;
          vector<int>b;
          while (n--)
          {
              cin>>t;
              b.emplace_back(t);
              ++a[t];
          }
          t=*max_element(all(a));
          for(auto&e:b){
              if(a[e]==t)cout<<e<<' ';
          }
          cout<<bp<<t;
          return 0;
      }   
