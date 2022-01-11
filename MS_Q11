vector<string> generate(int N)
{
	vector<string> ans;
	for(int i=1;i<=N;i++)
	{
	    int x=i;
	    string s="";
	    while(x)
	    {
	        int r=x%2;
	        if(r==0)
	        s="0"+s;
	        else
	        s="1"+s;
	        x/=2;
	    }
	    ans.push_back(s);
	}
	return ans;
}
