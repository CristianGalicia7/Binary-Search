# Binary-Search
// CGalicia Binary Search Program 02/23/2015
#include <cstdio>
#include <cstring>
#include <iostream>

using namespace std;

bool BinarySearch(char *array[10], int size, char* value)
{
	
if (size == 0)
		return false;
	else
	{
		int i, j, k;
		i = 0;
		j = size-1;
		
		while (i < j)
		{
			k = (i+j) / 2;
		if ((strcmp(value,array[k])>0))
		j = k-1;
		else if ((strcmp(value,array[k+1])>=0))
			i = k+1;
		else 
			i = j = k;
		}
		return (!strcmp(value,array[i])) ? true : false;
	}
}


int main()
{
	//sorted array of strings 
	char* strings [10] ={"BALL", "LAMB", "LAST", "LOST", "LOST", "MALL", "MOST", "TALL"};
	//SEARCH FOR A STRING
	if (BinarySearch(strings, 10, "MOST"))
		cout<<"The word is found." << endl;
	else
		cout << "The word is not found," << endl;

	/*{declare variable to store # to search for?
	double guessnumber , ArrayName; 
	cout<<"Ok now please input a number (0-999) to search for : ";
	cin>> guessnumber; 
	//Call the BinarySearch Function
	if (BinarySearch(ArrayName, 50, guessnumber))
		cout<<"Your number:"<<guessnumber<<"was founf!" <<endl;
	else
		cout<<"I'm sorry your number was not found!" <<endl;}
		                                                   */
}


