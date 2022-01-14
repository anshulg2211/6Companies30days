class Graph
{
    int V;
    list<int>*adj;
    public:
    Graph(int V)
    {
        this->V=V;
        adj = new list<int>[V];
    }
    void addEdge(int v,int w)
    {
        adj[v].push_back(w);
    }
    vector<int> topoSort() 
	{
	    stack<int> s;
	    vector<int> vis(V,0);
	    for(int i=0;i<V;i++)
	    {
	        if(!vis[i])
	        {
	            dfs(i,vis,s);
	        }
	    }
	    vector<int> ans;
	    while(!s.empty())
	    {
	        ans.push_back(s.top());
	        s.pop();
	    }
	    return ans;
	}
	void dfs(int node,vector<int> &vis,stack<int> &s)
	{
	    vis[node]=1;
	    for(auto x: adj[node])
	    {
	        if(!vis[x])
	        dfs(x,vis,s);
	    }
	    s.push(node);
	}
    
};

class Solution{
    public:
    string findOrder(string dict[], int N, int K) {
        Graph g(K);
        for(int i=0;i<N-1;i++)
        {
            string a=dict[i],b=dict[i+1];
            for(int j=0;j<min(a.length(),b.length());j++)
            {
                if(a[j]!=b[j])
                {
                    g.addEdge(a[j]-'a',b[j]-'a');
                    break;
                }
            }
        }
        vector<int> topOrder = g.topoSort();
        string ans;
        for(int i=0;i<K;i++)
        {
            ans+=(topOrder[i]+'a');
        }
        return ans;
    }
};
