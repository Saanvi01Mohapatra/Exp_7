# Experiment 7
# AIM:
Array and string  Operations in C++
## Comparison Table

| Feature           | Array                                           | String                                       |
|-------------------|-------------------------------------------------|----------------------------------------------|
| **Definition**    | A collection of elements of the same type stored in contiguous memory locations. | A sequence of characters, often implemented as an array of characters with additional functionalities. |
| **Size**          | Fixed size, determined at creation.            | Dynamic size, can change in many languages. |
| **Mutability**    | Elements can be modified.                      | Mutable or immutable depending on the language. |
| **Access**        | Accessed via indices.                          | Characters accessed via indices; includes built-in methods for manipulation. |
| **Operations**    | Manual operations for sorting, searching, etc.  | Built-in methods for concatenation, substring extraction, searching, etc. |
| **Memory Management** | Manual memory management in languages like C/C++. | Automatic memory management in higher-level languages. |
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
## Strings:
#### Showing Strings
**Theory:**

Displaying a string involves simply presenting its content to the user. This operation is fundamental in programming and serves various purposes such as debugging, user feedback, and output generation. When you show a string, you typically output its content to the console or a user interface.

Key Points:

**Purpose**: To display or output the contents of a string to the user.
**Use Case** Debugging, logging, or displaying messages in a program.
**Implementation:** Generally involves calling a function or method that outputs the string to a screen or log file.
#### Reversing Strings
Theory:

Reversing a string involves creating a new string where the characters are in the opposite order compared to the original string. This operation is often used in algorithms, data processing, and sometimes in solving specific problems where the order of characters is significant.

Key Points:

Purpose: To reverse the sequence of characters in a string.
Use Case: Useful in algorithms, data manipulation, or when solving problems that require reversed data.
Implementation: Typically involves iterating over the string from the end to the beginning, or using built-in functions that reverse the order of characters.
#### Concatenating Strings
Theory:

Concatenating strings means joining two or more strings end-to-end to form a single, longer string. This operation is essential for constructing messages, generating dynamic content, or combining data from different sources.

Key Points:

Purpose: To combine multiple strings into one continuous string.
Use Case: Building messages, generating dynamic text, or merging data from different sources.
Implementation: Usually involves appending the characters of one string to another or using functions that handle string concatenation.
#### Checking Palindrome
Theory:

A palindrome is a string that reads the same forward and backward, such as "radar" or "level". Checking if a string is a palindrome involves comparing the string to its reverse. This operation is useful in various applications, including text processing and pattern recognition.

Key Points:

Purpose: To determine if a string is a palindrome.
Use Case: Used in text analysis, pattern matching, and certain algorithms where symmetry is a factor.
Implementation: Typically involves reversing the string and comparing it to the original. If both are identical, the string is a palindrome.

### Code 1:CALLING ARRAY
```
//Saanvi mohapatra
//entc B2
//23070123110
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
//Saanvi mohapatra
//entc B2
//23070123110
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
//Saanvi mohapatra
//entc B2
//23070123110
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
//Saanvi mohapatra
//entc B2
//23070123110
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
//Saanvi mohapatra
//entc B2
//23070123110
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
//Saanvi mohapatra
//entc B2
//23070123110
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
//Saanvi mohapatra
//entc B2
//23070123110
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

### Strings code 1:
```cpp
//Saanvi mohapatra
//entc B2
//23070123110
//experiment 7 strings1
#include <iostream>
#include<string>
using namespace std;
int main(){
    string a;
    cout<<"enter any word: ";
    cin>>a;
    cout<<" entered string is "<<a<<endl;
    return 0;
}
/*PS C:\Users\asus\Desktop\cds> cd "c:\Users\asus\Desktop\cds\arrayandstrings\" ; if ($?) { g++ strings1.cpp -o strings1 } ; if ($?) { .\strings1 }
enter any word: saii
 entered string is saii*/
```
### Strings code 2:
```cpp
//Saanvi mohapatra
//entc B2
//23070123110
//experiment 7
#include<iostream>
#include<string>
using namespace std;
int main()
{
    string a,b;
    cout<<"enter string1: ";
    cin>>a;
cout<<"enter string 2:";
    cin>>b;
    cout<<"CONCATENATION: "<<a+b;
    return 0;
}
/*PS C:\Users\asus\Desktop\cds\arrayandstrings> cd "c:\Users\asus\Desktop\cds\arrayandstrings\" ; if ($?) { g++ concatenatestr.cpp -o concatenatestr } ; if ($?) { .\concatenatestr }
enter string1: sai
enter string 2:sankar
CONCATENATION: saisankar*/
```
### Strings code 3:
```cpp
//Saanvi mohapatra
//entc B2
//23070123110
//experiment 7
#include<iostream>
#include<string>
using namespace std;
int main()
{
    string a;
    cout<<"enter string you want to reverse: ";
    cin>>a;
    int i;
    cout<<"Here is your reversed string:"<<endl;
    for(i=a.length()-1;i>=0;i--)
    
    {
        cout<<a[i];
    }
    return 0;
}
/*PS C:\Users\asus\Desktop\cds\arrayandstrings> cd "c:\Users\asus\Desktop\cds\arrayandstrings\" ; if ($?) { g++ revstring.cpp -o revstring } ; if ($?) { .\revstring }
enter string you want to reverse: sai
Here is your reversed string:
ias*/
```
### String Code 4:
```cpp
//Saanvi mohapatra
//entc B2
//23070123110
//experiment 7
#include<iostream>
#include<string>
using namespace std;
int main()
{
    string a;
    cout<<"enter a string: ";
    cin>>a;
    int n=a.length(),i,flag=0;
    for(i=0;i<a.length();i++)
    {
        if(a[i]==a[n-1])
        {
            flag=1;
        }
        n--;
    }
    if(flag==1)
    {
        cout<<a<<" is palindrome";
    }
    else
    {
        cout<<a<<" is not palindrome";
    }
}
/*PS C:\Users\asus\Desktop\cds\arrayandstrings> cd "c:\Users\asus\Desktop\cds\arrayandstrings\" ; if ($?) { g++ PALINDROME.cpp -o PALINDROME } ; if ($?) { .\PALINDROME }
enter a string: MALAYALAM
MALAYALAM is palindrome
PS C:\Users\asus\Desktop\cds\arrayandstrings> cd "c:\Users\asus\Desktop\cds\arrayandstrings\" ; if ($?) { g++ PALINDROME.cpp -o PALINDROME } ; if ($?) { .\PALINDROME }
enter a string: SEMICINDUCTOR
SEMICINDUCTOR is palindrome*/
```


## Conclusion:Array
Arrays are a fundamental data structure in C++ that allow you to store a fixed-size sequence of elements of the same type. Below is a brief explanation of key concepts related to arrays.

- **Declaration**: Specifies the type and size of an array.
  - Example: `int numbers[10];`

- **Initialization**: Assigns initial values to array elements, either during declaration or afterward.
  - Example: `int arr[5] = {1000, 2, 3, 17, 50};`

- **Accessing Elements**: Retrieves or modifies elements using an index.
  - Example: `int num = arr[3];`
## Conclusion Strings


- **Arrays** are fixed-size collections of elements of the same type stored in contiguous memory locations, allowing for direct access via indices and requiring manual management for resizing and operations.

- **Strings** are sequences of characters with dynamic sizing capabilities in many languages, often featuring built-in methods for common operations like concatenation and substring extraction.

- **Mutability** of arrays and strings depends on the language: arrays are generally mutable, while strings may be mutable or immutable.

- **Memory Management** varies: arrays often require manual management in lower-level languages, while strings typically benefit from automatic memory management in higher-level languages.
### Summary
