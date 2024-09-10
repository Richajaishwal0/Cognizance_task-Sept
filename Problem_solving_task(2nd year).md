# Preliminary task for 2nd year
## Task 1
## Code:
```bash
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
## Task 2
Code:
## 
```bash
  list_numbers = ['one', 'two', 'three', 'four', 'five', 'six', 'seven', 'eight', 'nine', 'ten','eleven', 'twelve', 'thirteen', 'fourteen', 'fifteen', 'sixteen', 'seventeen', 'eighteen', 'nineteen', 'twenty', 'twenty one', 'twenty two', 'twenty three', 'twenty four', 'twenty five', 'twenty six', 'twenty seven', 'twenty eight', 'twenty nine']
    
    if m == 0:
        return (f"{list_numbers[h-1]} o\' clock") 
    if m>0 and m<30:
        if m == 15:
            return (f"quarter past {list_numbers[h-1]}")
        elif m==1:
            return (f"{list_numbers[m-1]} minute past {list_numbers[h-1]}")
        else:
            return (f"{list_numbers[m-1]} minutes past {list_numbers[h-1]}")
    if m== 30:
        return (f"half past {list_numbers[h-1]}")
    if m>30 and m<60:
        if m == 45:
            return (f"quarter to {list_numbers[h]}")
        else:
            minute_rem = 60- m
            return (f"{list_numbers[minute_rem-1]} minutes to {list_numbers[h]}")

```
![image](https://github.com/user-attachments/assets/713ef0fb-c938-49c5-b789-dfc4dc17362e)
