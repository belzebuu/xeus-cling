
# Task1


```c++
#include "pch.h"
#include <iostream>
#include <string>
#include <sstream>
using namespace std;
int are(int w,int d);

int main()
{


cout<<are(5, 10);
  return 0;
   
}
int are(int weight,int deep)
{


        try {
        cin >> weight;
        cin >> deep;

        if (weight < 0 ||  deep<0)      //Try for negative value
        {

                throw 4.5;
                cout << "After throw (Never executed) \n";
            }

            if (deep > 15000)  //Try for max value, number is just an example
            {
                throw 10;

            }
            if (weight == 2)
            {                         
                throw 'A';      //Throwing character exception
            }
            if (deep == 3)        //Throwing float exception
            {
                throw 4.5;
            }
            return weight * deep;
        }

        catch (double w) {
            cout << "Exception Caught  for  input \n";
            cout << "Input is zero or float number \n";
        }
        catch (int max_value_exception) {
            cout << "Exception Caught for d \n";
        }
        catch (char ch)
        {
            cout << "\nCharacter exception caught.";
        }

}

```

# Task2


```c++
Cout << "Success!\n" ;          //Compiler erro
cout << "Success!\n; "         // Compiler error  missing "  Syntax error
cout << "Success " << !\n "    // Compiler error  
cout << success << '\n';       //  Compiler error syntac error
string res = 7; vector<int> v(10); v[5] = res; cout << " Success!\n " ;   // Compiler error , type errors
vector<int> v(10); v(5) = 7; if (v(5)!=7) cout << " Success!\n " ;   //Compiler error syntax error
if (cond) cout << " Success!\n " ; else cout << " Fail!\n " ;    //Compiler error, variable definition
bool c = false; if (c) cout << " Success!\n " ; else cout << " Fail!\n " ;  
string s = " ape " ; boo c = " fool " <s; if (c) cout << " Success!\n " ;   // compiler error 
string s = " ape " ; if (s== " fool " ) cout << " Success!\n " ;           //Logic error   
string s = " ape " ; if (s== " fool " ) cout < " Success!\n " ;           //Compiler error, logic error
string s = " ape " ; if (s+ " fool " ) cout < " Success!\n " ;           // Compiler error, logic error
vector<char> v(5); for (int i=0; 0<v.size(); ++i) ; cout << " Success!\n " ;   //

```

# Task5


```c++
double ctok(double c)
{
        double k = c + 273.15;
        try
        {
            if (k<0)
            {
                throw -1;
            }
            return k;
        }
        catch (int a)
        {
            cout << "K is less than zero";
            return 0;
        }
        
}

int main()
{
        
double c;
        cin >> c;
        try {
            
            if (c<=-273.15)      
            {
                throw 4.5;
            }
            double k = ctok(c);
            cout << k << '/n';
        }
        catch ( double d )
        {
            cout << "Inpuut value less than -273.15";
        }

}
```
