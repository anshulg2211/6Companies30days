int checkSum(Node* root,int sum,int &cnt)
{
    if(root==NULL)
    return 0;
    
    int sm = root->data+checkSum(root->left,sum,cnt)+checkSum(root->right,sum,cnt);
    if(sm==sum)
    cnt++;
    return sm;
}
int countSubtreesWithSumX(Node* root, int X)
{
	int cnt=0;
	checkSum(root,X,cnt);
	return cnt;
}
