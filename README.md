#include <bits/stdc++.h>

using namespace std;

int main()
{
    int s,n,x,y;
    cin>>s>>n;
    vector<pair<int,int>>dragon;
    for(int i=0; i<n; i++)
    {
        cin>>x>>y;
        dragon.push_back(make_pair(x,y));
    }
    sort(dragon.begin(),dragon.end());
     for(int j=0; j<n; j++)
    {
        if(dragon[j].first<s)
        {
             s+=dragon[j].second;
        }
        else
        {
             cout<<"NO"<<endl;
             return 0;
        }
    }
    cout<<"YES"<<endl;
    return 0;
}
