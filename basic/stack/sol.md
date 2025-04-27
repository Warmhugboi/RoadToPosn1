# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        stack<ll>st;
        int n;
        cin>>n;
        for(int i=0;i<n;++i){
            string x;
            cin>>x;
            if(x=="push"){
                int y;
                cin>>y;
                st.emplace(y);
            }
            else if(x=="pop" && !st.empty()){
                cout<<st.top()<<'\n';
                st.pop();
            }
            else cout<<"null\n";
        }

    }

# Sol_tull
