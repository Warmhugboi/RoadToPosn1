# Sol_top

        #include <bits/stdc++.h>
        using namespace std;
        #define ll long long
        #define ep emplace_back
        
        bool prime[int(1e6+1)];
        
        
        int main(){
            cin.tie(NULL)->sync_with_stdio(false);
            int n,k,l=0;
            cin>>n>>k;
            int r=n-1;
            vector<int>arr;
            prime[1]=1;
            for (int p = 2; p * p <= 1e6+1; p++) {
                if (prime[p] == false) {
                    for (int i = p * p; i <= 1e6+1; i += p)
                        prime[i] = true;
                }
            }
        
            for(int i=0;i<n;++i){
                int x;
                cin>>x;
                arr.ep(x);
            }
            while(r >= l){
                int sum=0, MA=INT_MIN;
                int mid = l+(r-l)/2;
                for(int i=0;i<mid;++i){
                    if(prime[arr[i]]==0)
                        ++sum;
                }
                MA=max(MA,sum);
                for(int i=0;i<n-mid-1;++i){
                    if(prime[arr[i]]==0){
                        --sum;
                    }
                    if(prime[arr[i+mid]]==0){
                        ++sum;
                    }
                    MA=max(MA,sum);
                }
                if(MA>=k)
                    r=mid-1;
                else
                    l=mid+1;
            }
            cout<<l;
        

        }
# Sol_tull
