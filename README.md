# HOWMANYZIPCODES
FINDS A CERTAIN NUMBER OF A CERTAIN ZIPCODE
#include <iostream>
#include <fstream>
#include <string>
#include <regex>
#include <cstdlib>	//for exit()

using namespace std;
bool regex_match(int z, int b)
{
	if (z == b)
		return true;
}

int main()
{
	int counter = 0;
	int TheZip = 77004;
	ifstream inputfile("real_acct.txt");


	inputfile.open("real_acct.txt");

	if (!inputfile)
	{
	cerr << "Uh oh, real_acct.txt could not be opened!" << endl;
	exit(1);

	}
	

	while (inputfile) // WHile in loop read each line and if we match the zipcode increment counter.
	{
	// read stuff from the file into a string and print it
	long long int Zipcodes;
	inputfile >> Zipcodes;
	regex_match(Zipcodes, TheZip);
	if (regex_match(Zipcodes, TheZip))
	counter++;
	
	
	}
	
	cout << counter << endl;
	return 0;
}
