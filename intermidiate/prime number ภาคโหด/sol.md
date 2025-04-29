# Sol_top

        #include <bits/stdc++.h>
        using namespace std;
        #define ll long long
        #define mp make_pair
        #define F first
        #define S second
        #define ep emplace_back
        #define pll pair<ll,ll>
        #define For(i,a) for(int i=0;i<a;++i)
        #define str string
        #define MOD int(1e6+3)
        #define MAXN int(1e6+5)



        int main() {
            cin.tie(NULL)->sync_with_stdio(false);
            ll n,q,sum=0;
            cin>>n>>q;
            map<ll,ll>m;
            for(int i=1;i<=n;++i){
                ll x;
                cin>>x;
                sum+=x;
                //cout<<'\n'<<sum<<' '<<i;
                m[sum]=i;
            }
            /*for(auto&i:m){
                cout<<i.first<<' '<<i.second<<'\n';
            }

            cout<<"\n\n";
            for(auto&i:m){

            }*/

            for(auto it=++m.begin();it!=m.end();++it){
                auto x=it,y=--it;
                if(x->S < y->S){
                    x->S=y->S;
                }
                ++it;
            }

        /*for(auto&i:m){
            cout<<i.first<<' '<<i.second<<'\n';
            }*/

        for(int i=0;i<q;++i){
                ll x;
                cin>>x;
                if(m.upper_bound(x)!=m.begin())
                    cout<<(--m.upper_bound(x))->second<<'\n';
                else  cout<<(m.upper_bound(x))->second -1<<'\n';
            }

        }

# Sol_tull
