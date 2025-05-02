# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        string x;
        cin>>x;
        int sum=0;
        for(auto&i:x){
            if(i<'a')
                sum++;
        }
        if(sum==0)
            cout<<"LowerCase";
        else if(sum==x.length())
            cout<<"UpperCase";
        else cout<<"MIX";
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
          bool up=true,down=true;
          cin>>k;
          for(auto&e:k){
                if(isupper(e)){
                      down=false;
                }else{
                      up=false;
                }
          }
          if(up and !down){
                cout << "UpperCase";
          }else if(!up and down){
                cout << "LowerCase";
          }else{
                cout<<"MIX";
          }
          return 0;
    }
