# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        string x;
        cin>>x;
        int sum=1, MA=-1;
        char track;
        for(int i=1;i<x.length();++i){
            if(x[i]!=x[i-1])
                sum=1;
            else
                sum+=1;
            if(sum>MA){
                MA=max(MA,sum);
                track=x[i];
            }
        }
        cout<<track<<'\n'<<MA;
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
          int s=1,m=1;
          char c=k[0];
          for(int i=1;i<k.size();++i){
                if(k[i]==k[i-1]){
                      ++s;
                }else{
                      s=1;
                }
                if(s>m){
                      m=s;
                      c=k[i];
                }
          }
          cout<<c<<'\n'<<m;
          return 0;
    }
