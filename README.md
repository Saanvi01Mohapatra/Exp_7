# Experiment 7
# AIM:
Array Operations in C++
## ARRAY
An array is a collection of elements, all of the same type, stored in contiguous memory locations. Arrays provide a way to efficiently store and access multiple values using a single variable name, with each value accessible via an index.
Sure! Below is a detailed explanation of array declaration, initialization, and accessing in C++.

## Declaring Arrays
To declare an array in C++, specify the type of elements and the number of elements required:
type arrayName[array_size];
type: Any valid C++ data type.
array_size: An integer constant greater than zero.

## Initializing Arrays
You can initialize array elements individually or in a single statement:
int arr[5] = {1000, 2, 3, 17, 50};
The number of values within braces { } must not exceed the declared array size.

## Accessing Array Elements
Access elements by indexing the array name with square brackets [ ]:
int num = arr[9]; // Accesses the 10th element
## Key Characteristics of Arrays
Fixed Size: The size of an array
is determined when it is declared and cannot be changed during runtime. If you need a dynamic size, consider using other data structures like lists or vectors.

Homogeneous Elements: All elements in an array must be of the same type, such as integers, characters, or floating-point numbers.

Indexed Access: Each element in an array can be accessed directly using an index. In most programming languages, indexing starts from 0. For example, in an array a with 5 elements, a[0] refers to the first element and a[4] refers to the last element.

Contiguous Memory Allocation: Arrays are stored in contiguous memory locations, which means that the elements are stored next to each other. This allows for efficient access and iteration through the array.

### Code 1:CALLING ARRAY
```
//Sai Sankar Jena
//23070123112
//Entc b2
#include<iostream>
using namespace std;
int main()
{
 int a[4]={51,65,84,96};
cout<< "array is "<< a[1];
return 0;
}
/*PS C:\Users\asus\Desktop\cds\arrayandstrings> cd "c:\Users\asus\Desktop\cds\arrayandstrings\" ; if ($?) { g++ array.cpp -o array } ; if ($?) {
 .\array }
array is 65*/
```
### Code 2:INITIALISING ARRAY
```
//Sai Sankar Jena
//23070123112
//Entc b2
#include<iostream>
using namespace std;
int main()
{
 int a[4]={51,65,84,96};
 int b[7]={1,2,3,5,8,88,9};
 int c[2]={89,37};
 cout<<" array a: ";
for(int i=0;i<4;i++){
    cout<<a[i]<<' ';}
cout<<endl;
cout<<"array b: ";
    for(int j=0;j<7;j++){
    cout<<b[j]<<' ';}
    cout<<endl;
    cout<<" array c: ";
    for(int k=0;k<2;k++){
    cout<<c[k]<<' ';}
    cout<<endl;

return 0;
}
/*PS C:\Users\asus\Desktop\cds\arrayandstrings> cd "c:\Users\asus\Desktop\cds\arrayandstrings\" ; if ($?) { g++ array2.cpp -o array2 } ; if ($?) { .\array2 }
 array a:  51 65 84 96 
array b: 1 2 3 5 8 88 9
 array c: 89 37*/
```

### Code 3:ELEMENTS IN ARRAY USING DEFINE
```
//Sai Sankar Jena
//23070123112
//Entc b2
#include <iostream>
#define SIZE 6
using namespace std;

int main() {
    int a[SIZE];

    
    cout << "Enter " << SIZE << " elements of array: ";
    for (int index = 0; index < SIZE; index++) {
        cin >> a[index];
    }
    cout << endl;

    
    cout << "Array elements are: ";
    for (int j = 0; j < SIZE; j++) {
        cout << a[j] << "  ";
    }
    cout << endl;

    return 0;
}
/*PS C:\Users\asus\Desktop\cds\arrayandstrings> cd "c:\Users\asus\Desktop\cds\arrayandstrings\" ; if ($?) { g++ array3.cpp -o array3 } ; if ($?) { .\array3 }
Enter 6 elements of array: 8
6
5
4
2
3

Array elements are: 8  6  5  4  2  3*/
```


### Code 4:REVERSED
```
//Sai Sankar Jena
//23070123112
//Entc b2
#include<iostream>
using namespace std;

int main() {
    int n, i, j=0, k, l;
    cout<<"Enter size of array: ";
    cin>>n;
    int a1[n], a2[n];


    
    for(i=0;i<n;i++) {
        cout<<"Enter element-"<<i+1<<": ";
        cin>>a1[i];
    }
   
    cout<<"\nArray given by user: ";
    for(l=0;l<n;l++) {
        cout<<a1[l]<<" ";
    }
    cout<<endl;
   
    for(k=n-1;k>=0;k--) {
       
       a2[n - 1 - k] = a1[k];
    }
    
    cout<<"Reversed array: "<<' ';
    for(l=0;l<n;l++) {
        cout<<a2[l]<<" ";
    }
}
/*PS C:\Users\asus\Desktop\cds\arrayandstrings> cd "c:\Users\asus\Desktop\cds\arrayandstrings\" ; if ($?) { g++ array4.cpp -o array4 } ; if ($?) { .\array4 }
Enter size of array: 2
Enter element-1: 5
Enter element-2: 6

Array given by user: 5 6
Reversed array:  6 5*/
```
### Code 5:POSITION
```
//Sai Sankar Jena
//23070123112
//Entc b2
#include<iostream>
#define MAX_SIZE 10
using namespace std;
int main() {
    int elem[MAX_SIZE];
    int i,n, j, num, flag=0, count=0;
    cout << "Enter size of the array : ";
    cin >> n;
    for(i=0;i<n;i++) {
        cout<<"Enter element-"<<i+1<<": ";
        cin>>elem[i];
    }
    cout<<"Enter element to be searched: ";
    cin>>num;
    for(j=0;j<n;j++) {
        if(elem[j]==num) {
            cout<<"Position of "<<num<<": "<<j+1<<endl;
            count++;
            flag=1;
        }
    }
    if(flag==0) {
        cout<<"Element not present";
    }
    else if(flag==1) {
        cout<<"Element is present: "<<count<<" times";
    }
}
/*PS C:\Users\asus\Desktop\cds\arrayandstrings> cd "c:\Users\asus\Desktop\cds\arrayandstrings\" ; if ($?) { g++ array5.cpp -o array5 } ; if ($?) { .\array5 }
Enter size of the array : 3
Enter element-1: 5
Enter element-2: 6
Enter element-3: 94
Enter element to be searched: 6
Position of 6: 2
Element is present: 1 times*/
```

### Code 6: SUM/AVG
```
//Sai Sankar Jena
//23070123112
//Entc b2
#include <iostream>
using namespace std;

#define SIZE 10

int main() {
int n; 
    float a1[SIZE]; 

    
    float sum = 0, avg;
cout << "Enter number of elements to use : ";
    cin >> n;
   
    for (int i = 0; i < n; i++) {

        cout << "Enter element-" << i + 1 << ": ";
        cin >> a1[i];
    }

   
    for (int j = 0; j < n; j++) {
        sum += a1[j];
    }
    

   
    avg = sum / n;

    
    cout << "Sum of elements = " << sum << endl;
    cout << "Average = " << avg << endl;

    return 0;
}
/*PS C:\Users\asus\Desktop\cds\arrayandstrings> cd "c:\Users\asus\Desktop\cds\arrayandstrings\" ; if ($?) { g++ array6.cpp -o array6 } ; if ($?) { .\array6 }
Enter number of elements to use : 2
Enter element-1: 3.2
Enter element-2: 2.3
Sum of elements = 5.5
Average = 2.75*/
/*Enter number of elements to use : 2
Enter element-1: 6
Enter element-2: 4
Sum of elements = 10
Average = 5*/
```
### Code 7: MAX MIN
```
//Sai Sankar Jena
//23070123112
//Entc b2
#include<iostream>
using namespace std;
int main() {
    int n, i, max=0;
    cout<<"Enter number of elements: ";
    cin>>n;
    int a[n];
    for(i=0;i<n;i++){
        cout<<"Enter element-"<<i<<": ";
        cin>>a[i];
    }
    for(i=0;i<n;i++){
        if(a[i]>max){
            max=a[i];
        }
    }
    int min=a[0];
    for(i=0;i<n;i++){
        if(min>a[i]){
            min=a[i];
        }
    }
    cout<<"Maximum: "<<max<<endl<<"Minimum: "<<min;
}
/*PS C:\Users\asus\Desktop\cds\arrayandstrings> cd "c:\Users\asus\Desktop\cds\arrayandstrings\" ; if ($?) { g++ array7.cpp -o array7 } ; if ($?) { .\array7 }
Enter number of elements: 2
Enter element-0: 6
Enter element-1: 5
Maximum: 6
Minimum: 5*/
```
### Summary



Arrays are a fundamental data structure in C++ that allow you to store a fixed-size sequence of elements of the same type. Below is a brief explanation of key concepts related to arrays.

- **Declaration**: Specifies the type and size of an array.
  - Example: `int numbers[10];`

- **Initialization**: Assigns initial values to array elements, either during declaration or afterward.
  - Example: `int arr[5] = {1000, 2, 3, 17, 50};`

- **Accessing Elements**: Retrieves or modifies elements using an index.
  - Example: `int num = arr[3];`



