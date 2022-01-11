class Solution
{
    public:
    //Function to calculate the span of stockâ€™s price for all n days.
    vector <int> calculateSpan(int price[], int n)
    {
       vector<int> ans(n);
       stack<int> s;
       for(int i=0;i<n;i++)
       {
           if(s.empty() || price[i] < price[s.top()])
           {
               s.push(i);
               ans[i] = 1;
               continue;
           }
           else if(price[i] >= price[s.top()])
           {
               ans[i] = 1;
               while(!s.empty() && price[s.top()] <= price[i])
               {
                   ans[i] += ans[s.top()];
                   s.pop();
               }
               s.push(i);
           }
       }
       return ans;
    }
};
