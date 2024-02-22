Array Rotation Left and Right
In this program we’ll be learning about Python program for rotation of elements of array – left and right to a specified number of times. An array is said to be right rotated if all the selected elements were  moved towards right by one position. The last element of array will become the first element of array after rotation and vice versa for left rotation. 

Example
Input :arr[5] = [10, 20, 30, 40, 50]
Output :
Right rotation by 1 position : 50 10 20 30 40
Left rotation by 1 position : 20 30 40 50 10
Method 1 :
In this method we will rotate the elements one by one by shifting them.

Declare a function leftRotate(arr, d, n)
Inside that function run a loop for range(d)
And call leftRotateOne(arr, n)
For function leftRotatebyOne(arr, n)
Store arr[0] in a variable say temp.
Run a loop for range(n-1), set arr[i] = arr[i+1]
At last set arr[n-1] to temp
Time and Space Complexity :
Time – Complexity : O(n*d)
Space – Complexity : O(1)
Method  1 : Code in Python
#Write a program for array rotation in Python

# Python3 program to rotate an array by
def leftRotate(arr, d, n):
    for i in range(d):
        leftRotatebyOne(arr, n)
 
# Function to left Rotate arr[] of size n by 1*/
def leftRotatebyOne(arr, n):
    temp = arr[0]
    for i in range(n-1):
        arr[i] = arr[i + 1]
    arr[n-1] = temp
         
 
# utility function to print an array */
def printArray(arr, size):
    for i in range(size):
        print ("% d"% arr[i], end =" ")
 
  
# Driver program to test above functions */
arr = [10, 20, 30, 40, 50, 60, 70]
leftRotate(arr, 2, 7)
printArray(arr, 7)
Output
30 40 50 60 70 10 20 
