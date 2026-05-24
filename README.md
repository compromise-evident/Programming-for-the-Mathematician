<!-- The shortest C++ intro right in the README, with deep and immediately useful samples below. Crunch files, infosec, or values of any size and precision, all at full speed. -->

* ```apt install g++ geany```
* Copy the following using the copy button.
* Paste it in Geany and save it as anything.cpp in a folder.

```text
//Hit F9 to compile. F5 to run.

/*This is a multi-line comment, where
you can write the version of your program,
describe what it does, and how to run it.*/

#include <iostream>
using namespace std;
int main()
{	int amps  = 3; //Your variable named "amps" is of type int, and is initialized to 3.
	int volts = 5;
	
	cout << "Total power: " << (amps * volts) << " watts.";
	
	//This is a comment. All your code goes here, within the 2 curly braces of main().
}

```

<br>
<br>

# Variables

Replace all your code with:

```text
//Hit F9 to compile. F5 to run.
//You should see 2 warnings: unused variables c and d.

#include <iostream>
using namespace std;
int main()
{	//Valid variable names: this_is_a_descriptive_variable_name_123, a, b, c_1, c_2_quantity ...
	
	int       a =  12; //Variable a is of type int.       Range: -2147483648 to 2147483647
	long long b = 200; //Variable b is of type long long. Range: -9223372036854775807 to 9223372036854775807
	double    c = 4.9; //Variable c is of type double.    Range: 15 digits total, just move the decimal point.
	char      d = 100; //Variable d is of type char.      Range: -128 to 127   Caution: this one is special.
	
	a *= 2; //a * 2
	a /= 2; //a / 2
	a += 2; //a + 1
	a -= 2; //a - 1
	a %= 5; //a mod 5
	a++;    //a incremented by 1
	a--;    //a decremented by 1
	
	a += (2 - 2);      //a + (2 - 2)
	a = (a * 2);       //a * 2
	a = ((a * 2) / 4); //a * 2 then a / 4
	//a is now 2 after all these operations.
	
	
	
	//if statements.
	if(a == 2)
	{	//The body of this "if" will be executed if a = 2.
		cout << "a = " << a << "\n";   //Prints also a new line.
		cout << "a + 1 = " << (a + 1); //Prints 3, but a is left at 2.
		/*You can replace the "==" comparison operator with:
		
		== (equal to)
		!= (not equal to)
		>  (greater than)
		<  (less than)
		>= (greater than or equal to)
		<= (less than or equal to) */
	}
	
	if((a == 2) && (b == 200))
	{	//Executes this body if a = 2 AND if b = 200.
	}
	
	if((a == 2) || (b == 200))
	{	//Executes this body if a = 2 OR if b = 200.
	}
	
	if((a == 0)
	|| (a != 0)
	|| (a >  0)
	|| (a <  0)
	|| (a >= 0)
	|| (a <= 0))
	{	//Executes this body if ANY are true. (The if
		//must be satisfied in order to execute its body).
	}
	
	if((a == 0)
	&& (a != 0)
	&& (a >  0)
	&& (a <  0)
	&& (a >= 0)
	&& (a <= 0))
	{	//Executes this body if ALL are true.
		//(This particular body will never run).
	}
	
	
	
	//if, else statement.
	if(a == 2)
	{	//Your code...
	}
	else
	{	//If the if is not satisfied, this body will ALWAYS run.
	}
	
	
	
	//if, else if statements.
	if(a == 2)
	{	//Your code...
	}
	else if(a == 3)
	{	//Your code...
	}
	else if(a == 4)
	{	//You can have as many "else if" as you want, even 1.
	}
	
	
	
	//if, else if, else statements.
	if(a == 2)
	{	//Your code...
	}
	else if(a == 3)
	{	//Your code...
	}
	else if(a == 4)
	{	//Your code...
	}
	else
	{	//If no cases are satisfied, this body will ALWAYS run.
		return 0; //Terminates the program. You can put return 0; anywhere.
	}
}

```

<br>
<br>

# Loops

Replace all your code with:

```text
//Hit F9 to compile. F5 to run.

#include <iostream>
using namespace std;
int main()
{	//This loop runs forever. It executes
	//its body, top-down, over and over.
	for(;;)
	{	if(5 == 5) {break;} //But this line breaks out, ending the loop.
		//The if's body is on the same line as the if, just for aesthetics.
	}
	
	//a is CREATED, a is COMPARED, a is UPDATED.
	for(int a = 0; a < 10; a++)
	{	//This is how your loops will mostly be written.
		//This for() loops while a < 10. And a is incremented.
		//This for() loops 10 times, and prints a for fun:
		cout << a << "\n";
		
		//A nested loop that runs forever.
		//But is broken out of, on round 1.
		//Note that although you broke out,
		//the outer loop still has you.
		//Nothing happens here. Carry on.
		for(;;) {break;}
		
		//Don't create another variable
		//named a here. It will conflict
		//with the a created by the for().
		
		//You don't need all 3 things for making a loop.
		//This forever loop is valid: for(int a = 0;;) {}
	}
	
	int loop_counter = 0;
	for(int a = 0; a < 10; a++)
	{	loop_counter++;
		
		continue; //Moves you to the beginning of the loop (shortens the loop).
		
		return 0; //This line is never executed because of the continue; above.
		
		//Everything created here will be destroyed once the looping is over, but
		//loop_counter is simply updated, and persists, because loop_counter was
		//created before this for() loop. This applies to ifs and any code body.
	}
	
	cout << "\nloop_counter = " << loop_counter << "\n";
}

```

<br>
<br>

# Arrays

Replace all your code with:

```text
//Hit F9 to compile. F5 to run.

#include <iostream>
using namespace std;
int main()
{	//Arrays are like an int, but many.
	int list[10] = {0};
	
	/*list is not a variable. It's an array. An array of variables.
	Each variable is of type int. These variables are called elements.
	list contains 10 elements, each one initialized to zero.
	
	Arrays are zero-indexed, so in normal speech
	list[0] contains the first element,
	list[9] contains the last  element, so
	
	the index of the FIRST element is 0,
	the index of the TENTH element is 9. */
	
	//The 5th element is set to 1000.
	list[4] = 1000;
	cout << "element 5 = " << list[4] << "\n\n";
	
	//a happens to coincide with the index of each element,
	//so a is printed. Then prints the value of each element.
	for(int a = 0; a < 10; a++)
	{	cout << a << " = " << list[a] << "\n";
	}
	
	
	
	/*Now go and solve any first few Project Euler problems and
	problem 104, USING BRUTE FORCE AND ONLY WHAT YOU KNOW SO FAR!
	
	If you can do that, you can do anything. Now sure, your GitHub
	is a résumé. But solving Project Euler puts you on a watchlist.
	In fact, the NSA reserves your number theory publication rights.
	
	And if you don't feel confident, you haven't played with the code;
	you simply don't love programming. But you can still utilize the
	samples below, and adjust variables where it says "YOUR CONTROLS".*/
}

```

<br>
<br>

# That's it! Samples & tips:

(This part is a Work in Progress, not yet sorted):

my mathematical stuff in WhatNot

RawVisual

no mouse

use long long for everything

backups

folders on desktop while building

colorscheme

versions

logs

what repos should look like

long long size = filesystem::file_size("my_file"); //Gets file size in bytes.

try to avoid system(), but def use it for quick stuff

"secure offline machines", RICIN

my solution to Project Euler 104,
in case the reader doesn't believe it can be done with
brute force and by using only these basic C++ variables, loops, and arrays...
variables which can't possibly handle 68,855-digit values.

<br>
<br>

### Copyright & licenses

By law, everything you do, automatically includes the license "all rights reserved".
That's copyright. It means you can sue someone for having the same thoughts.
But you can override this by including any license, such as the Unlicense.

Most github repos use licenses with conditions,
where if you took even a few lines of their code,
you must forever keep visiting their repo, downloading
their copyright notices, licenses, and names, and keep
including them in each and every one of your projects
containing those lines of code.
But still many repos are licensed under the Unlicense,
without conditions, and you can look through those repos
without the fear of being forever chained to a human and
its words, words enforced by handcuffs and prison time.

<br>
<br>

### Clean Room Reverse Engineering (CRRE)

* If your code has a restrictive license, person A reads your code and writes a description. (Dirty room).
* Person B reads that description and writes unique code. (Clean room).
* Now they can license their code under anything, such as the Unlicense.
* They can't sue you for having a copy of your own code.
* And most importantly, you can't sue them for having a copy of THEIR own code.
* Unless patents, they created a functionally identical, unrestricted version of your code for everyone.
