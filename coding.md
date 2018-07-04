# 07/04/2018
### 1. Two Sum
```java
public class Solution {
    public int[] twoSum(int[] nums, int target) {
        HashMap<Integer,Integer> map = new HashMap<Integer,Integer>();
        int[] res = new int[2];
        for(int i = 0; i < nums.length; i++){
            int num = target - nums[i];
            if(map.containsKey(num)){
                res[0] = map.get(num);
                res[1] = i;
                break;
            }
            map.put(nums[i],i);
        }
        return res;
    }
}
```
