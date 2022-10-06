/******************************************************************************
# project-3
I am a student trying to finish a project. I have been working at this thing for hours, and I have been slowly piecing away the bugs at this thing. I am still very new and barely know what I am doing. I would appreciate some help trying to get the l integer to stay the same after you input the number. I am also having issues getting paidBack and intrestPaid to be positive numbers instead of negative. Does anyone know any way to fix this? If so please let me know how so I can learn and not make the same mistake in the future.
*******************************************************************************/

#include <iostream>
#include <cmath>
#include <iomanip>

using namespace std;

int main()
{
    //int rate, l, n, monthlyPayment1, monthlyPayment2, paidBack, intrestPaid;
    
    double rate, l, n, monthlyPayment1, monthlyPayment2, paidBack, intrestPaid;
    
    //n can be integer
    
    cout<< " Whats the loan amount? ";
    cin>> l;
    cout<< " What is the monthly intrest rate? ";
    cin>> rate;
    cout<< " How many payments have you made? ";
    cin>> n;

// monthy payment = rate x (1 +rate)^n / ((1+rate)^n-1)         x L


    monthlyPayment1= rate*pow(1+rate,n)/(pow(1+rate,n)-1);
    
    //pow(x, y)
    

    monthlyPayment2= monthlyPayment1* l;
    cout<< monthlyPayment2;
    
    intrestPaid= l-(monthlyPayment2*n);
    
    paidBack= intrestPaid- l;

    cout<< l<< endl<< rate<< endl<< n<< endl;
    cout<< monthlyPayment2<< endl<< paidBack<< endl<< intrestPaid;
    
return 0;
}
