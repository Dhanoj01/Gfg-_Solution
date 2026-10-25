## 01. Second Largest

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/second-largest3735/1?utm_source=chatgpt.com)

### Problem Description

**Task:** Given an array of positive integers arr[], return the second largest element from the array. If the second largest element doesn't exist then return -1.Note: The second largest element should not be equal to the largest element.Examples:Input: arr[] = [12, 35, 1, 10, 34, 1]

#### Examples

##### Example 1

- **Output:**
```text
-1
```
- **Explanation:** The largest element of the array is 10 and the second largest element does not exist.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (3)

#### Solution 1 (Java)

- **Submitted:** 2026-10-25 13:09:01
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    public int getSecondLargest(int[] arr) {
      
      int largest = 0;
      int secondLargest = 0;
      
      for(int i=0 ; i<arr.length ; i++)
      {
          
          if(arr[i] > largest)
          {
                secondLargest = largest;
                largest = arr[i];
          }
          
          else if(arr[i] < largest && arr[i] > secondLargest)
          {
              secondLargest = arr[i];
          }
      }
      
      return secondLargest==0?-1:secondLargest;
    }
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-10-25 12:58:10
- **Status:** Correct
- **Marks:** 0

```java
// User function template for C++
class Solution {
  public:
    // Function returns the second
    // largest elements
    int getSecondLargest(vector<int> &arr) {

        int n=arr.size();
       if(n<2)
       {
           return -1;
       }


       int first = -1;
       int second = -1;

       for(int i=0 ; i<n ; i++)
       {
           if(arr[i]>first)
           {
               second = first;
               first = arr[i];
           }
          else if(arr[i] != first && arr[i] > second)
           {
               second = arr[i];
           }
        }

        if(second == -1)
        {
            return -1;
        }

        return second;
    }
};
```

#### Solution 3 (Java)

- **Submitted:** 2024-12-31 20:36:44
- **Status:** Correct
- **Marks:** 2

```java
// User function template for C++
class Solution {
  public:
    // Function returns the second
    // largest elements
    int getSecondLargest(vector<int> &arr) {
        
        int n=arr.size();
       if(n<2)
       {
           return -1;
       }
       
       
       int first = -1;
       int second = -1;
       
       for(int i=0 ; i<n ; i++)
       {
           if(arr[i]>first)
           {
               second = first;
               first = arr[i];
           }
          else if(arr[i] != first && arr[i] > second)
           {
               second = arr[i];
           }
        }
        
        if(second == -1)
        {
            return -1;
        }
        
        return second;
    }
};
```

*Generated on: 25/10/2026, 13:30:35*