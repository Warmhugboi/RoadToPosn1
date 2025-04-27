# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        string s;
        cin>>s;
        int sum=0;
        for(auto&i:s){
            if(i>='a' && i<='z'){
                if(i=='a' or i=='e' or i=='i' or i=='o' or i=='u')
                    sum++;
            }
            else
                if(i=='A' or i=='E' or i=='I' or i=='O' or i=='U')
                    sum++;
        }
        cout<<sum;
        }

# Sol_tull
