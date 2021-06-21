#include <iostream>
#include <string>
#include <cmath>
#include <algorithm>
using namespace std;
int main()
{

	string emp_name[10000],name;
	char Gender[10000];
	int emp_salary[10000], emp_Age[10000],sal=0;
	int choice = 0, c = 0, s = 0, e = 0, a[100000] = { 0 };

	while (true)
	{
		cout << "Enter Your Choice:" << endl;
		cout << "1) Add new employee" << endl;
		cout << "2) Print All data of employee " << endl;
		cout << "3) Delete by age " << endl;
		cout << "4) Update Salary by name " << endl;
		cin >> choice;

		if (choice == 1)
		{
			
			cout << "Enter name: ";
			cin >> emp_name[c];
			cout << "Enter age: ";
			cin >> emp_Age[c];
			cout << "Enetr Salary: ";
			cin >> emp_salary[c];
			cout << "Enter gender (M/F): ";
				cin >> Gender[c];
				cout << endl;
			c++;
		}
		else if (choice == 2)
		{
			
	       for (int i = 0; i < c; i++)
    	   {
			  if (a[i]== 0)
		      {
		    	cout << emp_name[i] << " " << emp_Age[i] << " " << emp_salary[i] << " " << Gender[i] << endl<<endl<<endl<<endl;
	  	      }
	       }
		}
		else if (choice == 3)
		{
			cout << "Enetr Start and End Age "<<endl;
			cin >> s >> e;
			for (int i = 0; i < c; i++)
			{
				if (emp_Age[i] > s && emp_Age[i] < e)
					a[i]++;
			}
		}
		else if (choice == 4)
		{
			cout << "Enetr the name and Salary :";
			cin >>name>>sal;
			for (int i = 0; i < c; i++)
			{
				if (emp_name[i] == name)
				{
					emp_salary[i] = sal;
				}
			}
		}
	}
}
