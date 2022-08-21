# **T2A1-B - Workbook**  
**Name:** Wade Doolan  
**Student number:** 12678  

<hr>   

## **Question 1:**  

*Identify and explain the workings of TWO sorting algorithms and discuss and compare their performance/efficiency (i.e. Big O).*  

### The Bubble Sort algorithm  

The following python code is an implementation of the bubble sort algorithm:

```python
def bubble_sort(array):
    n = len(array)

    for i in range(n):

        already_sorted = True

        for j in range(n - i - 1):
            if array[j] > array[j + 1]:
               
                array[j], array[j + 1] = array[j + 1], array[j]

                already_sorted = False

        if already_sorted:
            break

    return array
```
(Real Python, 2020)

#### Algorithm description

Essentially, the bubble sort algorithm uses an iterative approach by looping through the elements in a list multiple times and comparing the value of each element with the value of the adjacent element. If the adjacent element's value is less than the current element's value, the elements' positions are swapped. This continues until all the elements have been sorted in ascending order. This process involves using nested loops, with the inner loop working to push the higher valued elements to the right after each iteration. The larger elements are bubbled up with each iteration (Real Python, 2020). The algorithm is explained in more detail below with an example.    

**Example:** using the bubble sort algorithm to sort elements in the following list ```python my_list = [1,7,3,9,2]```

The bubble sort algorithm involves:
1. accepting one argument, a list of values n elements long to be sorted. *In this case my_list.*
2. Once the list is passed into the function, the length of the list is assigned to the variable n. *The length on my_list is 5.*
3. The function then enters the outer loop, which is set to run from 0 to the last element's index value. *The last index value of my_list is 4.* 
4. A boolean variable 'already_sorted' is set to True, this is used to make the function more efficient by exiting early if all the elements are sorted.
5. The algorithm now enters the inner loop, which is set to run a reducing number of times with every iteration of the outer loop. *Therefore, the first iteration of the outer loop means the inner loop will run (n-i-1) or (5-0-1 = 4) times. The inner loop will start at index 0 and go up index 3 in my_list.* 
6. The purpose of the inner loop is to iterate through the elements and check if the value an element is greater than the value of the adjacent element. If it is then the elements are swapped. *The first complete run of the inner loop will result in 3, 7 and 9, 2 being swapped in my_list, with the 9 and 7 being shifted to the right of list*
7. If the elements are swapped, the variable 'already_sorted' is set as False to indicate to the outer loop that elements are still being sorted. *Since elements were swapped, 'already_sorted' is set to False.*
8. Once the inner loop has meet the required condition to exit (n-i-1), the algorithm begins the next iteration of the outer loop and so on until all the elements are sorted. *In the case of my_list, the inner loop has iterated 4 times and outer loop now begins the second iteration, starting the process for the inner loop over again; however, this time the inner loop will only iterate through the first three elements. That is (n-i-1) or (5-1-1 = 3) times. The process is repeated until my_list is sorted [1,2,3,7,9].*  

#### Algorithm performance






### The Quicksort algorithm  

The following python code is an implementation of the quicksort algorithm:

```python
from random import randint

def quicksort(array):
   
    if len(array) < 2:
        return array

    low, same, high = [], [], []

 
    pivot = array[randint(0, len(array) - 1)]

    for item in array:
    
        if item < pivot:
            low.append(item)
        elif item == pivot:
            same.append(item)
        elif item > pivot:
            high.append(item)

    return quicksort(low) + same + quicksort(high)
```
(Real Python, 2020)





<hr>  

## **Question 2:**  

*Identify and explain the workings of TWO search algorithms and discuss and compare their performance/efficiency (i.e. Big O).*  




<hr>  

## References  

