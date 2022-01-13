class Solution
{
	public:
    //Function to find if the given edge is a bridge in graph.
    bool check(vector<bool> &vis,vector<int> adj[],int node,int target)
    {
        if(node == target)
        return true;
        if(vis[node])
        return false;
        vis[node]=true;
        for(auto x:adj[node])
        {
            if(check(vis,adj,x,target))
            return true;
        }
        return false;
    }
    int isBridge(int V, vector<int> adj[], int c, int d) 
    {
        if(V<=2)
        return 1;
        vector<bool> vis(V,false);
        vis[c]=true;
        for(auto x:adj[c])
        {
            if(x != d && check(vis,adj,x,d))
            return 0;
        }
        return 1;
    }
};
