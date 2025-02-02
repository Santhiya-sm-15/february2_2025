# february2_2025
The problems that I solved today

1.Given an array nums, return true if the array was originally sorted in non-decreasing order, then rotated some number of positions (including zero). Otherwise, return false. There may be duplicates in the original array. Note: An array A rotated by x positions results in an array B of the same length such that A[i] == B[(i+x) % A.length], where % is the modulo operation.

Code:
class Solution {
    public boolean check(int[] nums) {
        int cnt=0,i;
        for(i=1;i<nums.length;i++)
        {
            if(nums[i-1]>nums[i])
                cnt++;
        }
        if(nums[nums.length-1]>nums[0])
            cnt++;
        return cnt<=1;
    }
}

2.An array is considered special if every pair of its adjacent elements contains two numbers with different parity. You are given an array of integers nums. Return true if nums is a special array, otherwise, return false.

Code:
class Solution {
    public boolean isArraySpecial(int[] nums) {
        int i;
        for(i=1;i<nums.length;i++)
        {
            if(nums[i]%2==nums[i-1]%2)
                return false;
        }
        return true;
    }
}
