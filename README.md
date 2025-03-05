[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/AqLe5c87)


# 1.Climbing Stairs

CODE:

```
public:
    int climbStairs(int n) {
        if (n == 1) return 1; 
        if (n == 2) return 2; 

        int first = 1; 
        int second = 2; 
        int current;

        for (int i = 3; i <= n; ++i) { 
            current = first + second; 
            first = second; 
            second = current; 
        }
        
        return second; 
    }
```
OUTPUT:

![image](https://github.com/user-attachments/assets/3c76287a-dcf4-434c-a152-6fc019dda4ea)

# 2.Maximum Subarray

CODE:

```
class Solution {
public:
    int maxSubArray(vector<int>& nums) {
        int maxSum = nums[0], currentSum = nums[0];
        
        for (int i = 1; i < nums.size(); ++i) {
            currentSum = max(nums[i], currentSum + nums[i]);
            maxSum = max(maxSum, currentSum);
        }
        
        return maxSum;
    }
};
```

OUTPUT:

![image](https://github.com/user-attachments/assets/e8bb69e3-937e-49f4-9a16-20c029115bee)

# 3.House Robber

CODE:

```
class Solution {
public:
    int rob(vector<int>& nums) {
        int n = nums.size();
        if (n == 0) return 0;          
        if (n == 1) return nums[0];    

        int prev2 = 0;                 
        int prev1 = nums[0];          

        for (int i = 1; i < n; ++i) {
            int current = max(prev1, prev2 + nums[i]);  
            prev2 = prev1;              
            prev1 = current;         
        }

        return prev1;                
    }
};
```
OUTPUT:

![image](https://github.com/user-attachments/assets/82b7a6ad-d0c4-4dad-841d-613a4e44925d)

# 4. 

CODE:

```
public:
    int maxProfit(vector<int>& prices) {
        int minPrice = INT_MAX; // Initialize minimum price to a very large value
        int maxProfit = 0; // Initialize maximum profit to 0
        
        for (int price : prices) {
            if (price < minPrice) {
                minPrice = price; // Update minimum price if a lower price is found
            } else if (price - minPrice > maxProfit) {
                maxProfit = price - minPrice; // Calculate profit and update maxProfit if it's higher
            }
        }
        
        return maxProfit; // Return the maximum profit
    }
```

OUTPUT:

![image](https://github.com/user-attachments/assets/0976898e-26c9-4291-9660-006685559a8e)


