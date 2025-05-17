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
    
    
    
    int main() {
        cin.tie(NULL)->sync_with_stdio(false);
        ll n,q,sum=0;
        cin>>n>>q;
        map<ll,ll>m;
        for(int i=1;i<=n;++i){
            ll x;
            cin>>x;
            sum+=x;
            //cout<<'\n'<<sum<<' '<<i;
            m[sum]=i;
        }
        /*for(auto&i:m){
            cout<<i.first<<' '<<i.second<<'\n';
        }
    
        cout<<"\n\n";
        for(auto&i:m){
    
        }*/
    
        for(auto it=++m.begin();it!=m.end();++it){
            auto x=it,y=--it;
            if(x->S < y->S){
                x->S=y->S;
            }
            ++it;
        }
    
       /*for(auto&i:m){
           cout<<i.first<<' '<<i.second<<'\n';
        }*/
    
       for(int i=0;i<q;++i){
            ll x;
            cin>>x;
            if(m.upper_bound(x)!=m.begin())
                cout<<(--m.upper_bound(x))->second<<'\n';
            else  cout<<(m.upper_bound(x))->second -1<<'\n';
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
    #include <sstream>
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
    #define val(i,j) (i>=0 and i<n and j>=0 and j<m)
    
    signed main(){
        cin.tie(nullptr)->sync_with_stdio(false);
        int n,q;
        cin>>n>>q;
        vector<int>a(n);
        inv(a)
        while (q--)
        {
            cin>>n;
            int cnt=0;
            for(auto&e:a){
                n-=e;
                if(n>=0){
                    ++cnt;
                }else{
                    break;
                }
            }
            cout<<cnt<<bp;
        }
        
        return 0;
    }   
