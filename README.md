# dsa-rotatedarray
This code is rotating array by k place , taking k as input.
code:
#include <iostream>
using namespace std;

void rotate(int a[], int x,int k) {
    int temp[x];
    for (int i = 0; i < x; i++) {
        int newindex = (i + k) % x;
        temp[newindex] = a[i];
    }
    for (int i = 0; i < x; i++) {
        a[i] = temp[i];
    }
}

int main() {
    int x;
    cout << "enter the length of array : ";
    cin >> x;
   
    int a[x];
   
    cout << "enter the elements of array ..." << endl;
    for (int i = 0; i < x; i++) {
        cout << "enter : ";
        cin >> a[i];
    }
   
    cout << "before rotation : " << endl;
    for (int i = 0; i < x; i++) {
        cout << a[i] << " ";
    }
    cout << endl;
   
   int k;
   cout<<"enter the key to ratated array : ";
   cin>>k;
    rotate(a, x,k);
   
    cout << "after rotated by " <<x<<" places : " << endl;
    for (int i = 0; i < x; i++) {
        cout << a[i] << " ";
    }
    cout << endl;
   
    return 0;
}

output : 
enter the length of array : 3
enter the elements of array ...
enter : 1
enter : 2
enter : 3
before rotation : 
1 2 3 
enter the key to ratated array : 2
after rotated by 3 places : 
2 3 1 
