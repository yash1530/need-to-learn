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
    ******************************************************************************************
    #include <bits/stdc++.h>
using namespace std;

bool isPrime(int n)
    {
        if(n==0|| n==1)
         return false;
         for(int i=2;i*i<=n;i++)
         {
             if(n%i==0)
             return false;
         }
         return true;
    }
vector<int>primeProduct(long long L, long long R){
        // code here
       // long long int ans=1;
        long long int mod=1000000007;
        vector<int>v;
        for(auto i=L;i<=R;i++)
        {
            if(isPrime(i))
            {
                v.push_back(i);
                
            }
            //ans=(ans*i)%mod;*/
            
        }
        return v;
    }
int main()
{ 
    long long int L,R;
    cin>>L>>R;
    vector<int>v=primeProduct(L,R);
    for(auto it:v)
    {
        cout<<it<<" ";
    }
    
}
        
	



