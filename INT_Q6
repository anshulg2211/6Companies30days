class Solution {
public:
    int findInMountainArray(int target, MountainArray &mountainArr) {
        int peak=0;
        int n=mountainArr.length();
        int l=0,r=n-1;
        while(l<r)
        {
            int mid=(l+r)/2;
            if(mountainArr.get(mid+1)>mountainArr.get(mid))
            l=mid+1;
            else
            r=mid;
        }
        peak=l;
        int elem=mountainArr.get(peak);
        //cout<<peak;
        if(target>elem)
            return -1;
        if(target==elem)
            return peak;
        l=0;
        r=peak;
        while(l<r)
        {
            int mid=(l+r)/2;
            int ele=mountainArr.get(mid);
            if(ele==target)
                return mid;
            else if(ele>target)
                r=mid;
            else
                l=mid+1;
        }
        if(peak==n-2)
        {
            if(target==mountainArr.get(n-1))
                return n-1;
            else
                return -1;
        }
        l=peak+1;
        r=n-1;
        while(l<r)
        {
            int mid=(l+r)/2;
            int ele=mountainArr.get(mid);
            if(ele==target)
                return mid;
            else if(ele>target)
                l=mid+1;
            else
                r=mid;
        }
        if(target==mountainArr.get(n-1))
            return n-1;
        return -1;
    }
};
