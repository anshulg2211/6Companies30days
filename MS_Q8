class Solution
{
    public:
    //Function to connect nodes at same level.
    void connect(Node *root)
    {
       queue<Node*> q;
       q.push(root);
       while(!q.empty())
       {
           int x=q.size();
           while(x--)
           {
               Node* temp = q.front();
               q.pop();
               if(x==0)
               temp->nextRight=NULL;
               else
               temp->nextRight=q.front();
               
               if(temp->left)
               q.push(temp->left);
               if(temp->right)
               q.push(temp->right);
           }
       }
       
    }    
      
};
