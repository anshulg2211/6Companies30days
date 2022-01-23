int convert(string s)
{
    int ans=0;
    for(int i=0;i<s.length();i++)
    {
        ans=ans*10+(s[i]-'0');
    }
    return ans;
}
int missingNumber(const string& str)
{
    int n=str.length();
    if(n==1)
    return -1;
    int ans;
    bool b=false;
    int k;
    for(int i=1;i<=min(6,n);i++)
    {
        int prev=-1;
        k=i;
        for(int j=0;j<n;j+=k)
        {
            int num=convert(str.substr(j,i));
            
            if(num!=0 && (int)log10(num)<(int)log10(num+1))
            i++;
            else if(num!=0 && (int)log10(num)<(int)log10(num+2) && j+i<n)
            {
                int x=convert(str.substr(j+i,i));
                if(x!=num+1)
                {
                    int y=convert(str.substr(j+i,i+1));
                    if(y==num+2)
                    {
                        if(!b)
                        {
                            b=true;
                            ans=num+1;
                        }
                        else
                        return -1;
                        i++;
                        continue;
                    }
                    else
                    break;
                }
            }
            if(num>9 && (int)log10(num-1)<(int)log10(num) && k!=i)
            k++;
            if(prev==-1)
            prev=num;
            else
            {
                if(prev+1==num)
                {
                    prev=num;
                }
                else if(prev+2==num)
                {
                    ans=prev+1;
                    prev=num;
                    if(!b)
                    b=true;
                    else
                    return -1;
                }
                else
                break;
            }
        }
    }
    if(b)
    return ans;
    return -1;
}
