# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    #define ep emplace_back
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        ll n,k;
        cin>>n>>k;
        vector<ll>arr;
        for(int i=0;i<n;++i){
            ll x;
            cin>>x;
            arr.ep(x);
        }
        sort(arr.begin(), arr.end());
        for(int i=1;i<n;++i){
            arr[i]+=arr[i-1];
        }
        if(binary_search(arr.begin(),arr.end(), k)==true)
            cout<<lower_bound(arr.begin(), arr.end(), k)-arr.begin()+1;
        else cout<<lower_bound(arr.begin(), arr.end(), k)-arr.begin();
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
          int n,k,t,s=0;
          cin>>n>>k;
          priority_queue<int,vector<int>,greater<int>>pq;
          while (n--)
          {
                cin>>t;
                pq.emplace(t);
          }
          while (!pq.empty())
          {
                k-=pq.top();
                pq.pop();
                if(k<0)
                break;
                ++s;
          }
          cout<<s;
          return 0;
    }
