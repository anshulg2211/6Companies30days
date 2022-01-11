class Solution
{
    public:
    //Function to find list of all words possible by pressing given numbers.
    void solve(vector<char> ref[],int a[],int n,string s,int idx,vector<string>&ans)
    {
        if(idx==n)
        {
            ans.push_back(s);
            return;
        }
        int num = a[idx],len=ref[num].size();
        
        for(int i=0;i<len;i++)
        {
            solve(ref,a,n,s+ref[num][i],idx+1,ans);
        }
    }
    vector<string> possibleWords(int a[], int N)
    {
        vector<string> ans;
        vector<char> ref_str[] = {
            {},
            {},
            {'a','b','c'},
            {'d','e','f'},
            {'g','h','i'},
            {'j','k','l'},
            {'m','n','o'},
            {'p','q','r','s'},
            {'t','u','v'},
            {'w','x','y','z'}
        };
        solve(ref_str,a,N,"",0,ans);
        return ans;
        
    }
};
