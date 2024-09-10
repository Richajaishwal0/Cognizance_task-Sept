# Preliminary task for 2nd year
## The code for determining the number of pairs of array elements that have a difference equal to the target value is given below:
```
def pairs(k, arr):
    arr_set = set(arr)
    count = 0
    for i in arr:
        if (i + k) in arr_set:
            count += 1
        if (i - k) in arr_set:
            count += 1
    return count // 2
```
