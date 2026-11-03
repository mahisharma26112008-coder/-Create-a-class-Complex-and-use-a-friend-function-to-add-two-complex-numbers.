# -Create-a-class-Complex-and-use-a-friend-function-to-add-two-complex-numbers.


#include<iostream>
using namespace std;

class complex{
    private:
    int real,img;

    public:
    void input(){
        cout<<"enter real and imaginary number: ";
        cin>>real>>img;
    }

    friend complex add(complex c1,complex c2);
    friend void display(complex c);
};

complex add(complex c1,complex c2){
    complex c3;
    c3.real=c1.real+c2.real;
    c3.img=c1.img+c2.img;
    return c3;
}

void display(complex c){
    cout<<c.real<<"+"<<c.img<<"i";
}

int main(){
    complex c1,c2,c3;

    c1.input();
    c2.input();

    c3=add(c1,c2);

    cout<<"addition : ";
    display(c3);

    return 0;
}
