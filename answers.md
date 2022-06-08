# Big O Answers

## Snippet 1 -
### Big O: This would be O(n).
### Explanation:the time increases proportionally to the size of the input
```python
def largest(array, value):
  for item in array:
    if item > value:
      return False
  return True 
```


## Snippet 2 -
### Big O: this would be O(2n)
### Explanation: The input is iterated through two individual times but not compounded.

```python
def info_dump(customers):
  
  print('Customer Names:')
  for customer in customers: 
    print(customer['name'])
  
  print('Customer Locations:')
  for customer in customers: 
    print(customer['country'])
  
```

## Snippet 3 -
### Big O: O(1)
### Explanation: Regardless of input size, the algo is only ran once.

```python
def first_element_is_red(array):
  return array[0] == 'red' 
```

## Snippet 4 -
### Big O: O(n^2)
### Explanation: Here the array is enumerated seperatley in each listm then the second loop travels through the entire array at each step of the first loop.

```python
def duplicates(array):
  for index1, item1 in enumerate(array):
    for index2, item2 in enumerate(array):
      if index1 == index2:
        continue
      if item1 == item2:
        return True
  return False
``` 

## Snippet 5 -
### Big O: O(n^2) 
### Explanation:the first loop is ran O(n) independent of inner loop, the inner loop runs O(n) dependant on outerloop .

```python
words = ['chocolate', 'coconut', 'rainbow']
endings = ['cookie', 'pie', 'waffle']

for word in words:
  for ending in endings:
    print(word + ending)

```

## Snippet 6 -
### Big O: O(n)
### Explanation: the for loop is only ran one time per intput. increases linearly.

```python
numbers = [1,2,3,4,5,6,7,8,9,10]

def print_array(array):
  for item in array:
    print(item)

```

## Snippet 7 -
### Big O: O(n^2)
### Explanation: for every element in the foor loop. The while loop runs indefinitley until the paramaters are not met
### in other words for loop depend on condition of while loop to step

```python
# this is insertion sort
def insertionSort(arr): 
  for i in range(1, len(arr)): 
    key = arr[i] 
    j = i-1
    while j >=0 and key < arr[j] : 
      arr[j+1] = arr[j] 
      j -= 1
    arr[j+1] = key 
```

## Snippet 8 -
### Big O: O(n^2)
### Explanation: O(n) loop inside O(n) loop

```python
for i in range(len(my_list)):
  min_idx = i
  for j in range(i+1, len(my_list)):
      if my_list[min_idx] > my_list[j]:
          min_idx = j

  my_list[i], my_list[min_idx] = my_list[min_idx], my_list[i]
```
