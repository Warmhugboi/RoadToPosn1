# Sol_top

    #include <bits/stdc++.h>
    using namespace std;
    #define ll long long
    #define ep emplace_back
    
    int main(){
        cin.tie(NULL)->sync_with_stdio(false);
        vector<pair<string,int>>arr;
        arr.ep("M",1000);
        arr.ep("CM",900);
        arr.ep("D",500);
        arr.ep("CD",400);
        arr.ep("C",100);
        arr.ep("XC",90);
        arr.ep("L",50);
        arr.ep("XL",40);
        arr.ep("X",10);
        arr.ep("IX",9);
        arr.ep("V",5);
        arr.ep("IV",4);
        arr.ep("I",1);
        int n;
        cin>>n;
        int i=0;
        string ans;
        while(n >= 1){
            if(n >= arr[i].second){
                ans+=arr[i].first;
                n-=arr[i].second;
            }
            else
                ++i;
        }
        cout<<ans;

    }

# Sol_tull
    #include <iostream>
    #include <string>
    using namespace std;
    
    string intToRoman(int num) {
        string romanNumerals[] = {
            "M", "CM", "D", "CD", "C", "XC", "L", "XL", "X", "IX", "V", "IV", "I"
        };
        int values[] = {
            1000, 900, 500, 400, 100, 90, 50, 40, 10, 9, 5, 4, 1
        };
        string result = "";
        for (int i = 0; i < 13; i++) {
            while (num >= values[i]) {
                result += romanNumerals[i];
                num -= values[i];
            }
        }
        return result;
    }
    
    int main() {
        int n;
        cin >> n;
        if (n >= 1 && n <= 3999) {
            cout << intToRoman(n) << endl;
        }
        return 0;
    }
    
