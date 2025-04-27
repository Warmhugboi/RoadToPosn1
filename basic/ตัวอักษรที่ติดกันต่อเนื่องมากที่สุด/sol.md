# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        string x;
        cin>>x;
        int sum=1, MA=-1;
        char track;
        for(int i=1;i<x.length();++i){
            if(x[i]!=x[i-1])
                sum=1;
            else
                sum+=1;
            if(sum>MA){
                MA=max(MA,sum);
                track=x[i];
            }
        }
        cout<<track<<'\n'<<MA;
    }

# Sol_tull
