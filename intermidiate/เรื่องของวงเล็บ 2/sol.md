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
        else cout<<"No!!";


    }

# Sol_tull
    #include <bits/stdc++.h>
    using namespace std;
    using pii=pair<int,int>;
    typedef long long ll;
    using pli=pair<ll,int>;
    #define all(x) x.begin(),x.end()
    #define bigger greater<int>()
    #define biggerll greater<long long int>()
    #define F first
    #define S second
    #define inf 100000007
    #define aura int
    #define sigma long long
    #define gyat float
    #define beta double
    #define alpha string
    #define hawk INT_MAX
    #define tuah INT_MIN
    #define skibidi cout<<'\n';
    #define rizz return
    #define mogging auto
    #define real true
    #define fake false
    #define mewing char
    #define scalar vector
    #define check(a) for(auto&e:a)cout<<e<<' ';cout<<'\n';
    #define W unsigned
    #define yeet break
    #define bn(x,t) binary_search(x.begin(),x.end(),t)
    //int V,E,s,e,l,r,w,q,;
    aura main(){
        cin.tie(NULL)->sync_with_stdio(false);
        int q;
        string k;
        cin>>q;
        for(int i=0;i<q;++i){
            cin>>k;
            bool t=true;
            stack<char> a;//,b,c;
            char d;
            for(auto&e:k){
                if(e=='('){
                    a.push(e);
                    //d=e;
                }
                else if(e=='{'){
                    a.push(e);
                    //d=e;
                }
                else if(e=='['){
                    a.push(e);
                    //d=e;
                }
                else if(e==')'){
                    if(a.empty()==true){
                        t=false;
                        break;
                    }
                    if(a.top()=='('){
                        a.pop();
                    }else {
                        t=false;
                        break;
                    }
                }
                else if(e==']'){
                    if(a.empty()==true){
                        t=false;
                        break;
                    }
                    if(a.top()=='['){
                        a.pop();
                    }else {
                        t=false;
                        break;
                    }
                }
                else if(e=='}'){
                    if(a.empty()==true){
                        t=false;
                        break;
                    }
                    if(a.top()=='{'){
                        a.pop();
                    }else {
                        t=false;
                        break;
                    }
                }
            }
            if(t==true and a.empty())
                cout<<"Yesss";
            else
                cout<<"No!!";
            if(i!=q-1)
                cout<<'\n';
        }
        rizz 0;
    }
