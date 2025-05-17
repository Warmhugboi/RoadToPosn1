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
            if(i=='('){
                st.emplace(i);
            }
            if(i==')'){
                if(st.empty()){
                    tr = false;
                    break;
                }
                else st.pop();
            }
        }
        if(!st.empty())
            tr=false;
        if(tr==true) cout<<"Yesss";
        else cout<<"No";

    }

# Sol_tull
    #include <iostream>
    #include <vector>
    #include <queue>
    #include <stack>
    #include <algorithm>
    #include <string.h>
    #include <math.h>
    #include <map>
    #include <tuple>
    #include <set>
    #include <unordered_map>
    #include <unordered_set>
    #define int long long
    using namespace std;
    using pii=pair<int,int>;
    #define bp '\n'
    #define vp cout<<bp;
    #define ck(a) for(auto&e:a)cout<<e<<' ';cout<<'\n';
    #define inv(a) for(auto&e:a)cin>>e;
    #define all(a) a.begin(),a.end()
    const int MX=1e18;
    const int MN=-MX;
    #define F first 
    #define S second
    bool val(string a){
        stack<char>c;
        for(auto&e:a){
            if(e=='('){
                c.emplace(e);
            }else{
                if(c.empty() or c.top()!='('){
                    return false;
                }
                c.pop();
            }
        }
        return c.empty();
    }
    signed main(){
        cin.tie(nullptr)->sync_with_stdio(false);
        string k;
        cin>>k;
        cout<<(val(k)?"Yesss":"No!!");
        return 0;
    }   
