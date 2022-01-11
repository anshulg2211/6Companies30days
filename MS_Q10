class Solution
{
    public:
    //Function to find the maximum money the thief can get.
    int FindMaxSum(int arr[], int n)
    {
        if(n==1) 
        return arr[0];
        int t1 = arr[0];
        int t2 = max(t1,arr[1]);
        
        for(int i=2;i<n;i++)
        {
            int temp = t2;
            t2 = max(t2,t1+arr[i]);
            t1 = temp;
        }
        return t2;
    }
};
