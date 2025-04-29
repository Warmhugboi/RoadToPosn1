# Sol_top
 
#include <bits/stdc++.h>
using namespace std;
#define ll long long
#define ep emplace_back

bool so(pair<int,int>a, pair<int,int>b){
    if(a.first==b.first)
        return a.second > b.second;
    else return a.first < b.first;
}

int main(){
    cin.tie(NULL)->sync_with_stdio(false);
    int n;
    cin>>n;
    vector<pair<int,int>>arr;
    for(int i=0;i<n;++i){
        int x,y;
        cin>>x>>y;
        arr.ep(x,y);
    }
    sort(arr.begin(), arr.end(), so);
    for(auto&i:arr){
        cout<<i.first<<' '<<i.second<<'\n';
    }




}





}


# Sol_tull
