# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        string x;
        cin>>x;
        int sum=0;
        for(auto&i:x){
            if((i>='A' && i<='Z') or (i>='a' && i<='z') or (i>='0' && i<='9'))
                continue;
            else sum+=1;
        }
        if(sum==0)
            cout<<"Yes";
        else cout<<"No";

    }

# Sol_tull
