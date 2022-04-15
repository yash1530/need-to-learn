# need-to-learn
Sieve of Eratosthenes prime algorithms
prifix algorithms
#include<bits/stdc++.h>
using namespace std;
int seive(int n,int m)
{
    vector<int>prime(m+1,true);
    {
        prime[0]=false;prime[1]=false;
        for(int i=2;i*i<=m;i++)
        {
            if(prime[i]==true)
            {
                for(int j=i*i;j<=m;j=j+i)
                {
                    prime[j]=false;
                }
            }
        }
    }
    int count=0;
    for(int i=n;i<=m;i++)
    {
        
    if(prime[i]==true)
    {
        count=count+1;
        
    }
    }
    return count;
}
int main()
{
    int n,m;
    cin>>n>>m;
    cout<<seive(n,m);
}
