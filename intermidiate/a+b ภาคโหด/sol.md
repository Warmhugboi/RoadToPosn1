
# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        string a,b,c;
        int sum=0;
        cin>>a>>b;
        if(a.length()>b.length())
        {
            string x=a;
            a=b;
            b=x;
        }
        //b.insert(0,"0");
        while(a.length()<b.length())
        {
            a.insert(0,"0");
        }
        c=a;

        for(int i=a.length()-1;i>=0;--i)
        {
            c[i]=((int)a[i]-48)+(int)b[i]+sum;
            sum=0;
            if((int)c[i]-48>9)
            {
                c[i]=(int)c[i]-10;
                ++sum;
            }
        }
        if(sum>0)
            c.insert(0,"1");
        cout<<c;

    }

# Sol_tull
    #include <bits/stdc++.h>
    using namespace std;
    typedef long long ll;
    using pii=pair<int,int>;
    #define ll unsigned long long
    #define inf 1000000007
    #define all(a) a.begin(),a.end()
    #define F first
    #define S second
    int main()
    {
        cin.tie(NULL)->sync_with_stdio(false);
        string a,b;
        cin>>a>>b;
        ll n=a.size(),m=b.size();
        ll mnl=min(n,m),mxl=max(n,m);
        reverse(all(a));
        reverse(all(b));
    if(a.size()>b.size()){
        for(ll i=0;i<mxl;++i){
            //int temp;
            if(i!=mxl-1){
                if(i<mnl){
                    ll t1=a[i]-'0',t2=b[i]-'0';
                    if(t1+t2>9)
                    {
                        a[i]=t1+t2+'0'-10;
                        ++a[i+1];
                    }else a[i]=t1+t2+'0';
                }
                if(a[i]>'9'){
                    a[i]-=10;
                    ++a[i+1];
                }
            }else{
                if(i<mnl){
                    ll t1=a[i]-'0',t2=b[i]-'0';
                    if(t1+t2>9)
                    {
                        //cout<<t1+t2<<'\n';
                        a[i]=t1+t2+'0'-10;
                        a+="1";
                    }else a[i]=t1+t2+'0';
                }
                if(a[i]>'9'){
                    a[i]-=10;
                    ++a[i+1];
                }
            }
        }
            reverse(all(a));
            cout<<a;
    }else{
        for(ll i=0;i<mxl;++i){
            if(i!=mxl-1){
                if(i<mnl){
                    ll t1=a[i]-'0',t2=b[i]-'0';
                    if(t1+t2>9)
                    {
                        b[i]=t1+t2+'0'-10;
                        ++b[i+1];
                    }else b[i]=t1+t2+'0';
                }
                if(b[i]>'9'){
                    b[i]-=10;
                    ++b[i+1];
                }
            }else if(i==mxl-1){
                if(i<mnl){
                    ll t1=a[i]-'0',t2=b[i]-'0';
                    if(t1+t2>9)
                    {
                        b[i]=t1+t2+'0'-10;
                        b+="1";
                    }else b[i]=t1+t2+'0';
                }
                if(b[i]>'9'){
                    b[i]-=10;
                    ++b[i+1];
                }
            }
        }
            reverse(all(b));
            cout<<b;
    }
    /*
        bitset<5> a(9);
        //cin>>a;
        a;
        cout<<a;*/
        return 0;
    }

