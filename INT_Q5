class Solution {
public:
    bool solve(vector<int>&nums,int m,int sum)
    {
        int cur_sum=0;
        for(int i=0;i<nums.size();i++)
        {
            if(nums[i]>sum)
            return false;
            if(cur_sum+nums[i]<=sum)
            {
                cur_sum+=nums[i];
            }
            else
            {
                cur_sum=0;
                i--;
                if(m>1)
                m--;
                else
                return false;
            }
        }
        return true;
    }
    int splitArray(vector<int>& nums, int m) {
        int maxSum=accumulate(nums.begin(),nums.end(),0);
        if(m==1)
        return maxSum;
        int minSum=maxSum/m;
        int ans=INT_MAX;
        while(minSum<maxSum)
        {
            int midSum=(minSum+maxSum)/2;
            if(solve(nums,m,midSum))
            {
                ans=min(ans,midSum);
                maxSum=midSum;
            }
            else
            {
                minSum=midSum+1;
            }
        }
        return ans;
    }
};
