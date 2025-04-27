# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        queue<ll>q;
        int n;
        cin>>n;
        for(int i=0;i<n;++i){
            string x;
            cin>>x;
            if(x=="push"){
                int y;
                cin>>y;
                q.emplace(y);
            }
            else if(x=="pop" && !q.empty()){
                cout<<q.front()<<'\n';
                q.pop();
            }
            else cout<<"null\n";
        }

    }

# Sol_tull
