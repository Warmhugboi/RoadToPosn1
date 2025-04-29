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
