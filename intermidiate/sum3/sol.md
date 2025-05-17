# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        ll n;
        cin>>n;
        cout<<(n*(n+1))/2;
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
    #define bp '\n'\
    #define vp cout<<bp;
    #define ck(a) for(auto&e:a)cout<<e<<' ';cout<<'\n';
    const int MX=1e18;
    const int MN=-MX;
    #define F first 
    #define S second
    signed main(){
        cin.tie(nullptr)->sync_with_stdio(false);
        int n;
        cin>>n;
        cout<<(n&1?(n+1)/2*n:n/2*(n+1));
        return 0;
    }   
