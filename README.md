# Writing a C++ function to swap pointers
Write a C++ function *swap_pointers* that takes two integer pointers as input and swaps the values that they are point to 

## Method 1: Using arithmetic
```
void swap_pointers(int* ptr1, int* ptr2){
  *ptr1 = *ptr1 + *ptr2; 
  *ptr2 = *ptr1 - *ptr2; 
  *ptr1 = *ptr1 - *ptr2;
}
```
Explanation: 
- assume ptr1 holds the value '5'
- assume ptr2 holds the value '10'
- *ptr1 = *ptr1 + *ptr2;  //now ptr1 holds the value 15
- *ptr2 = *ptr1 - *ptr2;  //ptr2 = ptr1 (5)
- *ptr1 = *ptr1 - *ptr2;  //ptr1 = ptr2 (10)
<br>

*NOTE: this method doesn't use a temporary variable, and the code does not swap the pointers themselves; it swaps the values at the memory locations the pointers are pointing to.

<br>

## Method 2: Using a temp variable
```
void swap_pointers(int** ptr1, int** ptr2) {
    int temp = *ptr1;
    *ptr1 = *ptr2;
    *ptr2 = temp;
}
```
