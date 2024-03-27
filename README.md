Toggle each characters in a string
In this article we will learn how to write a C++ program to toggle each character in a string. Toggling characters means to convert lower case characters to upper case characters and upper case characters to lower case characters. This can be simply achieved by using ASCII values as there is a difference of 32 between lower case and upper case alphabets ASCII values.

length of string without using strlen
Algorithm:
Initialize the variables.
Accept the input.
Initiate a for loop and terminate it at the end of string.
Toggle each character using ASCII values.
Print toggled string.
 
Method 1
Run
#include <iostream>
#include <string.h>
using namespace std;
 
int main()
{
    //Initializing variable.
    char str[100];
    int i;
  	
    //Accepting input.
    cout<<"Enter the String: ";
    gets(str);
  	
  	//Initializing for loop.
  	for (i = 0; str[i]!='\0'; i++)
  	{
  	    //Toggling characters.
  	    if(str[i] >= 'A' && str[i] <= 'Z') { str[i] = str[i] + 32; } else if(str[i] >= 'a' && str[i] <= 'z')
            {
  	      str[i] = str[i] - 32;
	    }		
  		
  	}

  	cout<<"\nToggled string: "<<str<<endl; //Printing toggled string.
  	
  	return 0;
}
Output:
Enter the String: PREPinsta
Toggled string: prepINSTA
Method 2
The Logic is same here we are using the ASCII value

Initialize the variables.
Initiate a for loop.
Toggle each character.
Terminate the loop.
Print toggled string.
Run
#include <iostream>
#include <string.h>
using namespace std;

int main() {

    // Initializing variable.

    char str[100];
    int i;

   // Accepting input.
   cout << "Please Enter any String: ";    
   gets(str);
for (int i = 0; str[i] != '\0'; i++) {
if (str[i] >= 'A' && str[i] <= 'Z')
str[i] = str[i] + 'a' - 'A';
else if (str[i] >= 'a' && str[i] <= 'z')
            str[i] = str[i] + 'A' - 'a';     
}    
cout << "Toggled string: " << str;  
// Print toggled string.     return 0; }
Please Enter any String: Root
Toggled string: rOOT
Method 3
This program is the same as above, but this time we are using the While Loop

Run
#include <iostream>
#include <string.h>
using namespace std;
int main() {

    char Str1[100];
    int i;

    cout << "Please Enter any String to Toggle :  ";    gets(Str1);    i = 0;    while (Str1[i] != '\0') {        if (Str1[i] >= 'a' && Str1[i] <= 'z') {            Str1[i] = Str1[i] - 32;        } else if (Str1[i] >= 'A' && Str1[i] <= 'Z') {
            Str1[i] = Str1[i] + 32;
        }
        i++;
    }

    cout << "The Given String after Toggling Case of all Characters = " << Str1;
    return 0;

}
Please Enter any String to Toggle : Root
The Given String after Toggling Case of all Characters = rOOT
