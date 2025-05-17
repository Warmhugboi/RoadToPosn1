# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    #define ep emplace_back

    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        int n;
        cin>>n;
        vector<int>a;
        vector<int>b;
        bool visit[n];
        for(auto&i:visit) i=0;

        for(int i=0;i<n;++i){
            int x;
            cin>>x;
            if(x%2==0){
                a.ep(x);
                visit[i]=1;
            }
            else b.ep(x);

        }
        int j=a.size()-1, k=b.size()-1;
        for(int i=0;i<n;++i){
            if(visit[i]==1){
                cout<<a[j]<<' ';
                --j;
            }
            else {
                cout<<b[k]<<' ';
                --k;
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
        vector<int>a(n),odd,even;
        for(int i=0;i<n;++i){
            cin>>a[i];
            if(a[i]&1){
                odd.emplace_back(i);
            }else{
                even.emplace_back(i);
            }
        }
        int l=0,r=odd.size()-1;
        while (l<r)
        {
            swap(a[odd[l++]],a[odd[r--]]);
        }
        l=0,r=even.size()-1;
        while (l<r)
        {
            swap(a[even[l++]],a[even[r--]]);
        }
        ck(a)
        return 0;
    }
