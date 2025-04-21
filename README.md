#include <iostream>
using namespace std;

// Generic Linear Search Function
template <typename T>
int linearSearch(const T array[], int size, T key) {
    for (int i = 0; i < size; i++) {
        if (array[i] == key)
            return i; // Return index if found
    }
    return -1; // Return -1 if not found
}

int main() {
    // Testing with int array
    int intArray[] = {1, 3, 5, 7, 9};
    int intKey = 7;
    cout << "Index of " << intKey << " in int array: " 
         << linearSearch(intArray, 5, intKey) << endl;

    // Testing with double array
    double doubleArray[] = {1.1, 3.3, 5.5, 7.7, 9.9};
    double doubleKey = 5.5;
    cout << "Index of " << doubleKey << " in double array: " 
         << linearSearch(doubleArray, 5, doubleKey) << endl;

    // Testing with string array
    string strArray[] = {"apple", "banana", "cherry", "date", "elderberry"};
    string strKey = "cherry";
    cout << "Index of \"" << strKey << "\" in string array: " 
         << linearSearch(strArray, 5, strKey) << endl;

    return 0;
}
