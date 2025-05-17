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
        unordered_set<int>s={2,3,5,7,11,13,17,19,23,29,31,37,41,43,47,53,59,61,67,71,73,79,83,89,97,101,103,107,109,113,127,131,137,139,149,151,157,163,167,173,179,181,191,193,197,199,211,223,227,229,233,239,241,251,257,263,269,271,277,281,283,293,307,311,313,317,331,337,347,349,353,359,367,373,379,383,389,397,401,409,419,421,431,433,439,443,449,457,461,463,467,479,487,491,499,503,509,521,523,541,547,557,563,569,571,577,587,593,599,601,607,613,617,619,631,641,643,647,653,659,661,673,677,683,691,701,709,719,727,733,739,743,751,757,761,769,773,787,797,809,811,821,823,827,829,839,853,857,859,863,877,881,883,887,907,911,919,929,937,941,947,953,967,971,977,983,991,997};
        signed main(){
            cin.tie(nullptr)->sync_with_stdio(false);
            int t,n,k;
            vector<int>a;
            cin>>n>>k;
            for(int i=0;i<n;++i){
                cin>>t;
                if(s.count(t)){
                    a.emplace_back(i);
                }
            }
            int ans=a[k-1]-a[0]+1;
            for(int i=k;i<a.size();++i){
                ans=min(ans,a[i]-a[i-k+1]+1);
            }
            //ck(a)
            cout<<ans;
            return 0;
        }   
