# sum-of-range
Write a C++ code with a function named "sum" that takes two integer arguments, call them "first" and "last", and returns as its value the sum of all the integers between first and last inclusive. Always remember, your program will calculate the sum between first and last, even if the last is bigger than the first. 


#include <iostream>
using namespace std;

int rev(int x){
    int rem , revNum = 0;
    int y = x;

    while(x!=0){
        rem = x % 10;
        revNum = (revNum*10) + rem;
        x = x / 10;
    }

    int s = 0;
    while(y!=0){
        s = s + (y % 10);
        y = y/10;
    }
    cout << "Sum of the reverse number: " << s << endl;
    return revNum;

}


int main(){

    int num;
    cout << "Enter a number: ";
    cin >> num;
    int r = rev(num);
    cout << "Reverse Number: " << r << endl;
    return 0;
}
