class Solution {
public:
    int numberOfBoomerangs(vector<vector<int>>& points) {
        int n=points.size();
        unordered_map<int,int> m;
        int ans=0;
        for(int i=0;i<n;i++)
        {
            for(int j=0;j<n;j++)
            {
                if(i==j)continue;
                int dis = pow(points[i][0]-points[j][0],2)+pow(points[i][1]-points[j][1],2);
                m[dis]++;
            }
            for(auto x:m)
            {
                ans+=x.second*(x.second-1);
            }
            m.clear();
        }
        
        return ans;
        
    }
};
