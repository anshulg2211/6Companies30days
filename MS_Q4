class Solution
{   
    public: 
    //Function to return a list of integers denoting spiral traversal of matrix.
    vector<int> spirallyTraverse(vector<vector<int> > matrix, int r, int c) 
    {
       vector<int> ans;
       int direction=1,right=c,down=r,left=0,up=0;
       while(ans.size()<r*c)
       {
           if(direction==1)
           {
               for(int i=left;i<right;i++)
               {
                   ans.push_back(matrix[up][i]);
               }
               right--;
               direction++;
           }
           else if(direction==2)
           {
               for(int i=up+1;i<down;i++)
               {
                   ans.push_back(matrix[i][right]);
               }
               down--;
               direction++;
           }
           else if(direction==3)
           {
               for(int i=right-1;i>=left;i--)
               {
                   ans.push_back(matrix[down][i]);
               }
               left++;
               direction++;
           }
           else if(direction==4)
           {
               for(int i=down-1;i>up;i--)
               {
                   ans.push_back(matrix[i][left-1]);
               }
               up++;
               direction=1;
           }
       }
       return ans;
       
    }
};
