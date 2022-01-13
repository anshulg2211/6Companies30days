class Solution{
public:
    int minSteps(int D){
        int cnt=0;
        int n=0;
        while(n<D)
        {
            n=n+1+cnt;
            cnt++;
        }
        if(n==D)
        return cnt;
        while((n-D)%2 == 1)
        {
            n=n+1+cnt;
            cnt++;
        }
        return cnt;
    }
};
