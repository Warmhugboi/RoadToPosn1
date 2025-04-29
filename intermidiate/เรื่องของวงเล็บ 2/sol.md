# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    #define ep emplace_back
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        string x;
        cin>>x;
        stack<int>st;
        bool tr = true;
        for(auto&i:x){
            if(i=='(' || i=='{' || i=='['){
                st.emplace(i);
            }
            if(i==')'){
                if(st.empty()){
                    tr = false;
                    break;
                }
                else {
                    if(st.top()=='(')
                        st.pop();
                    else {
                        tr=false;
                        break;
                    }

                }
            }
            if(i=='}'){
                if(st.empty()){
                    tr = false;
                    break;
                }
                else {
                    if(st.top()=='{')
                        st.pop();
                    else {
                        tr=false;
                        break;
                    }
                }
            }
            if(i==']'){
                if(st.empty()){
                    tr = false;
                    break;
                }
                else {
                    if(st.top()=='[')
                        st.pop();
                    else {
                        tr=false;
                        break;
                    }
                }
            }
        }
        if(!st.empty())
            tr=false;
        if(tr==true) cout<<"Yesss";
        else cout<<"No";


    }

# Sol_tull
