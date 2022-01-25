//Same as INT_Q5
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
    int shipWithinDays(vector<int>& weights, int days) {
        int maxSum=accumulate(weights.begin(),weights.end(),0);
        if(days==1)
        return maxSum;
        int minSum=maxSum/days;
        int ans=INT_MAX;
        while(minSum<maxSum)
        {
            int midSum=(minSum+maxSum)/2;
            if(solve(weights,days,midSum))
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
