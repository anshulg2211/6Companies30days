class Solution{

  public:
	int minDifference(int arr[], int n)  { 
	    int sum=accumulate(arr,arr+n,0);
	    bool dp[n+1][sum+1];
	    for(int i=0;i<=n;i++)  //making all possible sums from all subsets
	    {
	        dp[i][0]=true;
	    }
	    for(int i=1;i<=sum;i++)
	    {
	        dp[0][i]=false;
	    }
	    for(int i=1;i<=n;i++)
	    {
	        for(int j=1;j<=sum;j++)
	        {
	            if(arr[i-1]>j)
	            dp[i][j]=dp[i-1][j];
	            else
	            dp[i][j]=dp[i-1][j]||dp[i-1][j-arr[i-1]];
	        }
	    }
	    int ans=0;
	    for(int i=0;i<=sum/2;i++)  //sum/2 because min diff would be 0 if we divide sum equally
	    {
	        if(dp[n][i])
	        {
	            ans=i;
	        }
	    }
	    return sum-2*ans;
	} 
};
