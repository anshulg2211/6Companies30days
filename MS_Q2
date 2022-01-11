class Solution {
public:
    bool isCyclic(int v, vector<bool>&vis,vector<bool>&st,vector<vector<int>>& adj)
    {
        if(vis[v] == false)
        {
            vis[v] = true;
            st[v] = true;
    
            vector<int>::iterator i;
            for(i = adj[v].begin(); i != adj[v].end(); ++i)
            {
                if ( !vis[*i] && isCyclic(*i, vis, st,adj) )
                    return true;
                else if (st[*i])
                    return true;
            }
        }
        st[v] = false;  
        return false;
    }

	bool isPossible(int N, vector<pair<int, int> >& prerequisites) {
	    vector<bool> vis(N,false),st(N,false);
	    vector<vector<int>> adj(N);
	    int p = prerequisites.size();
	    for(auto x:prerequisites)
	    {
	        adj[x.second].push_back(x.first);
	    }
	    for(int i=0;i<N;i++)
	    {
	        if(isCyclic(i,vis,st,adj))
	        return false;
	    }
	    return true;
	}
};
