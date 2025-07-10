# googleSTEP

## File Descriptions

| File name             | Usage                                            | Command |
|-----------------------|--------------------------------------------------|---------|
| malloc_worst_fit.py        | malloc challenge using worst fit            |make run |
| malloc_best_fit.py         | malloc challenge using best  fit            |make run |
| malloc_2_bins.py           | malloc challenge using 2 bins + best fit    |make run |
| malloc_4_bins.py           | malloc challenge using 4 bins + best fit    |make run |
| malloc_14_bins.py          | malloc challenge using 14 bins+ best fit    |make run |
| malloc_14_bins_advanced.py | malloc challenge using 14 bins + larger bins|make run |
| malloc_25_bins.py          | malloc challenge using 25 bins              |make run |


# Homework
## Overview
Find the efficeint way to implment malloc function

## Algorithm
### best fit
Iterate from the free head, get the metadata that holds the size that is larger and closest to the size of the memory we are looking at.

### Result
| Challenge    | Time [ms] | Utilization [%] |
|--------------|-----------|------------------|
| Challenge 1  | 1185      | 70               |
| Challenge 2  | 398       | 40               |
| Challenge 3  | 591       | 50               |
| Challenge 4  | 7289      | 71               |
| Challenge 5  | 4950      | 74               |




### worst fit
Iterate from the free head, get the metadata that holds the size that is larger and largest size at this moment to the size of the memory we are looking at.

### Result
| Challenge    | Time [ms] | Utilization [%] |
|--------------|-----------|------------------|
| Challenge 1  | 1185      | 70               |
| Challenge 2  | 398       | 40               |
| Challenge 3  | 591       | 50               |
| Challenge 4  | 7289      | 71               |
| Challenge 5  | 4950      | 74               |


### 2 free bins
The issue we only use one linked list to take care of the size of the free memoery, where we need to iterate from the beginning, which takes time, so this time we have two different linked list that takes care of differnet range of size so we don't need to iterate the irrelative metadata. This time, a_bin represents the metadata which size is less than 1000, and b_bin represents the metadata which has 1000 and more than 1000 size of memory.

### Result
| Challenge    | Time [ms] | Utilization [%] |
|--------------|-----------|------------------|
| Challenge 1  | 1185      | 70               |
| Challenge 2  | 398       | 40               |
| Challenge 3  | 591       | 50               |
| Challenge 4  | 7289      | 71               |
| Challenge 5  | 4950      | 74               |

1674,70,1112,40,1364,51,36111,24,20815,24

### 4 free bins
In the same way, we increased the number of bins and each bin takes care of 1000 bytes of memory.

### 14 free bins
In the same way, we also divide bins into 100, 200, 300, ... 1000, 2000, 3000, 4000 because the possibility of asking the large size might be lower than that of small size.

### 24 free bins


