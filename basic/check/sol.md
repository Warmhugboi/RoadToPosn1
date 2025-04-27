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
            if(i<'a')
                sum++;
        }
        if(sum==0)
            cout<<"LowerCase";
        else if(sum==x.length())
            cout<<"UpperCase";
        else cout<<"MIX";
    }

# Sol_tull
