# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        int n;
        cin>>n;
        bool prime[n+1];
        for(auto&i:prime) i=0;
        cout<<2<<' ';
        for(int i=3;i<=n; ){
            for(int j=2;j*j<=i;++j){
                if(i%j==0)
                    prime[i]=1;
            }
            if(prime[i]==0)
                cout<<i<<' ';
            i+=2;
        }
    }

# Sol_tull
