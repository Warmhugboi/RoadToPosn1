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
