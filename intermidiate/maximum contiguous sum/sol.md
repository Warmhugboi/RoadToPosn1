# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    #define ep emplace_back
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        int n;
        cin>>n;
        ll sum=0, MA=INT_MIN;
        for(int i=0;i<n;++i){
            ll x;
            cin>>x;
            if(sum+x < 0){
                sum=0;
            }
            else
                sum+=x;
            MA=max(MA,sum);
        }
        cout<<MA;
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
    #define inv(a) for(auto&e:a)cin>>e;
    #define all(a) a.begin(),a.end()
    const int MX=1e18;
    const int MN=-MX;
    #define F first 
    #define S second
    signed main(){
        cin.tie(nullptr)->sync_with_stdio(false);
        int n,t,rn=0,mxsf=MN;
        cin>>n;
        while (n--)
        {
            cin>>t;
            rn+=t;
            if(rn>mxsf){
                mxsf=rn;
            }
            if(rn<0){
                rn=0;
            }
        }
        cout<<mxsf;
        return 0;
    }   
