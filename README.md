# Sub-array-with-0-sum
find and return whether the given array contains a non-empty subarray with a sum equal to 0
If the given array contains a sub-array with sum zero return 1, else return 0.

Approach:We keep adding the sum of the elements to the Hashmap. We return 1 if we find any element is 0 or sum so far is 0 or if we encounter sum which is already in the HashMap

Problem Constraints
1 <= |A| <= 100000
-10^9 <= A[i] <= 10^9




    public int solve(int[] A) {
    
        HashSet<Long> map=new HashSet<>();
        
        long sum=0;
        
        for(int i=0;i<A.length;i++){
            sum=sum+A[i];
            if(sum==0||A[i]==0||map.contains(sum)){
                return 1;
            }
            map.add(sum);
        }
        return 0;
    }
