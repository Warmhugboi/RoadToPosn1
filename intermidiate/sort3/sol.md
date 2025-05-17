# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    #define ep emplace_back

    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        int n;
        cin>>n;
        vector<ll>a, b;
        bool visit[n+1];
        for(auto&i:visit) i=0;
        for(int i=0;i<n;++i){
            ll x;
            cin>>x;
            if(x%2==0){
                a.ep(x);
                visit[i]=1;
            }
            else b.ep(x);
        }
        sort(a.begin(), a.end());
        sort(b.rbegin(), b.rend());
        int j=0,k=0;
        for(int i=0;i<n;++i){
            if(visit[i]==1){
                cout<<a[j]<<" ";
                ++j;
            }
            else {
                cout<<b[k]<<" ";
                ++k;
            }
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
        int l=0,r=0,n,t;
        cin>>n;
        vector<int>a(n),even,odd;
        for(auto&e:a){
            cin>>e;
            if(e&1){
                odd.emplace_back(e);
            }else{
                even.emplace_back(e);
            }
        }
        sort(all(even));
        sort(all(odd),greater<int>());
        for(auto&e:a){
            if(e&1){
                e=odd[l++];
            }else{
                e=even[r++];
            }
        }
        ck(a)
        return 0;
    }   
