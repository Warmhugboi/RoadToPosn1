# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    #define ep emplace_back
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        int n,m;
        cin>>n>>m;
        map<vector<int>,int>arr;
        for(int i=0;i<n;++i){
            vector<int>a;
            for(int j=0;j<m;++j){
                int x;
                cin>>x;
                a.ep(x);
            }
            arr[a]+=1;
        }
        int MA=INT_MIN;
        vector<int>ans;
        for(auto&i:arr){
            if(i.second > MA){
                ans=i.first;
                MA=i.second;
            }
        }
        for(auto&i:ans) cout<<i<<' ';

        cout<<'\n'<<MA;

        }

# Sol_tull
