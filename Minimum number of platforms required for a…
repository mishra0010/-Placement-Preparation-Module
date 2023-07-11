class Solution
{
    static int findPlatform(int arr[], int dept[], int n)
    {
        Arrays.sort(arr);
        Arrays.sort(dept);
        int i=0; // for arrival time
        int j=0; //for dept time
        int count=0;
        int max=0;
        while(i<n){
            if(arr[i]<=dept[j]){
                count++;
                i++;
                max=Math.max(max,count);
            }
            else{
                count--;
                j++;
            }
        }
        return max;
    }
    
}
