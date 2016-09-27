#include <iostream>

using namespace std;

void calcCounty(double total, double &county);
void calcState(double total, double &state);
void calcTotal(double county, double state, double &total);
void printData(double calcCounty,double calcState,double calcTotal);
void datainput(double total);

int main()
{

	double total;
	double county;
	double state;
	double calcCounty;
	double calcState;
	double calcTotal;

	cout << "Welcome to the total tax calculator program! " << endl;
	
	datainput(total);
	calcCounty(total, county);
	calcState(total, state);
	calcTotal(county, state, total);
	printData(county, state, total);

	cout << "Author: Jeffrey Sirimaturos \n";


	system("pause");
	return 0;
}


void datainput(double total)
{
	cout << "Enter the total sales for the month: ";
	cin >> total;
}

void calcCounty(double total, double &county)
{
	county = total * .02;
}

void calcState(double total, double &state)
{
	state = total * .04;
}

void calcTotal(double &county, double &state, double total)
{
	total = state + county;
}

void printData(double calcCounty,double calcState,double calcTotal)
{
	cout << "The county tax is $ " << calcCounty;
	cout << "The state tax is $ " << calcState;
	cout << "The total tax is $ " << calcTotal;
}

