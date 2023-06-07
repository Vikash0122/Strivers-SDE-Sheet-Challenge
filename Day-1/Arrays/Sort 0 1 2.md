# Sort 0 1 2 

Problem Link:- [Code Studio](https://takeuforward.org/data-structure/sort-an-array-of-0s-1s-and-2s/)
~~~~

void sort012(int *a, int n)
{
    int count=0;
        for(int i=0; i<n; i++)
        {
            if(a[i]==0)
            {
                swap(a[i],a[count]);
                count++;
            }
        }
        
        int count1=0;
        count1=count;
        for(int i=count; i<n; i++)
        {
            if(a[i]==1)
            {
                swap(a[i],a[count1]);
                count1++;
            }
        }
}
~~~~
