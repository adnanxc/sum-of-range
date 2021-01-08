# sum-of-range
Write a C++ code with a function named "sum" that takes two integer arguments, call them "first" and "last", and returns as its value the sum of all the integers between first and last inclusive. Always remember, your program will calculate the sum between first and last, even if the last is bigger than the first. 


#include <iostream>
#include <cmath>
using namespace std;

int sum(int first , int last){
    int s = 0;

    for(int i=first; i<=last; i++){

        s = s + i;
    }

    return s;
}

int main(){
    int a , b , temp = 0;
    cout << "Enter the first number: ";
    cin >> a;
    cout << "Enter the second number: ";
    cin >> b;
    if(a>b){
        temp = a;
        a = b;
        b = temp;
    }

    int x = sum(a , b);

    if(temp>abs(a)){
        for(int i=b; i>=a; i--){
            cout << i << " + ";
        }
    }

    else{
        for(int i=a; i<=b; i++){
            if(i<0){
                cout << "(" << i << ") + ";
            }
            else{
                cout << i << " + ";
            }

        }
    }

    cout << "\b\b= " << x;

    return 0;
}
