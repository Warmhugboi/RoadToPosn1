# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    #define ep emplace_back
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        vector<pair<string,int>>arr;
        arr.ep("M",1000);
        arr.ep("CM",900);
        arr.ep("D",500);
        arr.ep("CD",400);
        arr.ep("C",100);
        arr.ep("XC",90);
        arr.ep("L",50);
        arr.ep("XL",40);
        arr.ep("X",10);
        arr.ep("IX",9);
        arr.ep("V",5);
        arr.ep("IV",4);
        arr.ep("I",1);
        int n;
        cin>>n;
        int i=0;
        string ans;
        while(n >= 1){
            if(n >= arr[i].second){
                ans+=arr[i].first;
                n-=arr[i].second;
            }
            else
                ++i;
        }
        cout<<ans;

    }

# Sol_tull
