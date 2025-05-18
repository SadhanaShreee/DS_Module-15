# Ex14 Heap Tree
## DATE: 25-03-2025
## AIM:
To write a C function to delete an element in a Heap Tree.

## Algorithm
1. Start
2. Find the index of the element num in the array.
3. Swap the element to be deleted with the last element in the array.
4. Decrease the array size (size) by 1.
5. Start heapifying from the last non-leaf node (index size/2 - 1).
6. Call heapify() to restore the heap property for each node.
7. End  

## Program:
```
Program to delete an element in a Heap Tree
Developed by: SADHANA SHREE B
RegisterNumber: 212223230177

void deleteRoot(int array[], int num)
{

  int i;
  for(i=0;i<size;i++){
      if(num==array[i]){
          break;
      }
  }
  swap(&array[i],&array[size-1]);
  size-=1;
  for(int i=size/2-1;i>=0;i--){
      heapify(array,size,i);
  }
}

```

## Output:

![Screenshot 2025-05-18 123519](https://github.com/user-attachments/assets/71582314-637b-4d2e-b213-fc63f9ec8ba2)


## Result:
Thus, the function to delete an element in a Heap Tree is implemented successfully.
