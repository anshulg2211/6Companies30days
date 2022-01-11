void swap(int *a,int *b)
{
    *a+=*b;
    *b=*a-*b;
    *a=*a-*b;
}

void rotate(int n,int a[][n])
{
    for(int i=0;i<n;i++)  //taking transpose
    {
        for(int j=i+1;j<n;j++)
        {
            swap(&a[i][j],&a[j][i]);
        }
    }
    int k=n-1;
    for(int i=0;i<n;i++) //reversing columns
    {
        for(int j=0;j<n;j++)
        {
            if(j<k)
            {
                swap(&a[j][i],&a[k][i]);
                k--;
            }
        }
        k=n-1;
    }
    
}
