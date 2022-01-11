class Solution
{
    public:
    //Function to find unit area of the largest region of 1s.
    int findMaxArea(vector<vector<int>>& grid) {
        int ans=0;
        for(int i=0;i<grid.size();i++)
        {
            for(int j=0;j<grid[0].size();j++)
            {
                int cnt=0;
                if(grid[i][j] == 1)
                {
                    dfs(grid,i,j,cnt);
                    ans=max(ans,cnt);
                }
            }
        }
        return ans;
    }
    void dfs(vector<vector<int>> &grid,int i,int j, int &cnt)
    {
        if(i>=grid.size() || i<0 || j>=grid[0].size() || j<0 || grid[i][j] == 0)
        return;
        cnt++;
        grid[i][j]=0;
        dfs(grid,i-1,j,cnt);
        dfs(grid,i-1,j+1,cnt);
        dfs(grid,i,j+1,cnt);
        dfs(grid,i+1,j+1,cnt);
        dfs(grid,i+1,j,cnt);
        dfs(grid,i+1,j-1,cnt);
        dfs(grid,i,j-1,cnt);
        dfs(grid,i-1,j-1,cnt);
    }
};
