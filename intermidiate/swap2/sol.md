# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    #define ep emplace_back

    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        int n;
        cin>>n;
        vector<int>a;
        vector<int>b;
        bool visit[n];
        for(auto&i:visit) i=0;

        for(int i=0;i<n;++i){
            int x;
            cin>>x;
            if(x%2==0){
                a.ep(x);
                visit[i]=1;
            }
            else b.ep(x);

        }
        int j=a.size()-1, k=b.size()-1;
        for(int i=0;i<n;++i){
            if(visit[i]==1){
                cout<<a[j]<<' ';
                --j;
            }
            else {
                cout<<b[k]<<' ';
                --k;
            }
        }
    }

# Sol_tull
