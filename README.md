# fast-cpp-csv-parser
Automatically exported from code.google.com/p/fast-cpp-csv-parser

## Instructions
Just include the library in your code. A note: the CSVReader and CSVLine is under io namespace.

The complete documentation is here https://code.google.com/p/fast-cpp-csv-parser/wiki/Documentation

I post here a few examples to show how it works.

### Examples
1. This example read a 3-column file without header and the types of each columns are: Integer, String, Integer respectively. Then just show the middle column.

```c++
#include <iostream>
#include "csv.h"
using namespace std;
using namespace io;
int main()
{
	CSVReader<3> in("example.csv");
	int year;
	string title;
	int ocurrences;
	while(in.read_row(year, title, ocurrences)){
		cout << title << endl;
	}
	return 0;
}
