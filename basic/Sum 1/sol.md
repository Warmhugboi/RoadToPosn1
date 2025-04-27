# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        ll l,r,k;
        cin>>l>>r>>k;
        ll sum=0;
        for(int i=l;i<=r;){
            sum+=i;
            i+=k;
        }
        cout<<sum;
    }

# Sol_tull
