# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        ll n,sum=0;
        cin>>n;

        for(int i=0;i<n;++i){
            ll x;
            cin>>x;
            if(x%2==0)
                sum++;
        }
        cout<<sum<<' '<<n-sum;
    }

# Sol_tull
