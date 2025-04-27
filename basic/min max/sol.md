# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        ll n,t;
        cin>>n;
        ll MA=INT_MIN, MI=INT_MAX;
        for(int i=0;i<n;++i){
            ll x;
            cin>>x;
            MA=max(MA,x);
            MI=min(MI,x);
        }
        cin>>t;
        if(t==1) cout<<MA;
        else cout<<MI;
    }

# Sol_tull
