##Find Minimum in Rotated Sorted Array II

38% Accepted

	Suppose a sorted array is rotated at some pivot unknown to you beforehand.

	(i.e., 0 1 2 4 5 6 7 might become 4 5 6 7 0 1 2).

	Find the minimum element.

	The array may contain duplicates.

	Have you met this question in a real interview? Yes
	Example
	Given [4,4,5,6,7,0,1,2] return 0

####Tags Expand
- Binary Search
- Divide and Conquer

####思路
- 构想极端情况 [1,1,1,1,1,1,1,1]
- 极端情况下 二分法也没用，找不到前面的，所以必须遍历
- 同理 Search in Rotated Sorted Array II 也是这么处理

```java
public class Solution {
    public int findMin(int[] num) {
        int min = num[0];
        for (int i = 1; i < num.length; i++) {
            if (num[i] < min)
                min = num[i];
        }
        return min;
    }
}
```