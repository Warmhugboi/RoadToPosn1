
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
