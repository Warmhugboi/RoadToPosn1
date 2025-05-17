# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    #define ep emplace_back
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        int n;
        cin>>n;
        vector<pair<int,int>>arr;
        for(int i=0;i<n;++i){
            int x,y;
            cin>>x>>y;
            arr.ep(x,1);
            arr.ep(y,0);
        }
        sort(arr.begin(), arr.end());
        int sum=0, MA=INT_MIN;
        for(auto&i:arr){
            if(i.second==1){
                sum++;
            }
            else
                sum--;
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
    vector<int>a(30,0);
    signed main(){
        cin.tie(nullptr)->sync_with_stdio(false);
        int n,l,r;
        cin>>n;
        while (n--)
        {
            cin>>l>>r;
            ++a[l];
            --a[r];
        }
        for(int i=1;i<30;++i)a[i]+=a[i-1];
        cout<<*max_element(all(a));
        return 0;
    }   
