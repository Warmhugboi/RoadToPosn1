# Sol_top
 
    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    #define ep emplace_back
    
    bool so(pair<int,int>a, pair<int,int>b){
        if(a.first==b.first)
            return a.second > b.second;
        else return a.first < b.first;
    }
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        int n;
        cin>>n;
        vector<pair<int,int>>arr;
        for(int i=0;i<n;++i){
            int x,y;
            cin>>x>>y;
            arr.ep(x,y);
        }
        sort(arr.begin(), arr.end(), so);
        for(auto&i:arr){
            cout<<i.first<<' '<<i.second<<'\n';
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
        int l,r,n,t;
        cin>>n;
        vector<pii>a(n);
        for(auto&[f,s]:a){
            cin>>f>>s;
        }
        sort(all(a),[&](const pii&l,const pii&r){
            return (l.F==r.F)?l.S>r.S:l.F<r.F;
        });
        for(auto&[f,s]:a){
            cout<<f<<' '<<s<<bp;
        }
        return 0;
    }   
