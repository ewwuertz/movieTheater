#movieTheater

#include "stdafx.h"
#include<iostream>
#include<string>
#include<iomanip>
using namespace std;

int main()
{
	int adultTickets, childTickets;
	double grossBoxoffice, netBoxoffice, paidToDistributer;
	string movieName;

	cout << "Enter the movie name: ";
	getline(cin, movieName);			//use getline() to allow for a spacebar in input

	cout << "Enter number of adult tickets sold: ";
	cin >> adultTickets;

	cout << "Enter number of child tickets sold: ";
	cin >> childTickets;

	grossBoxoffice = (adultTickets * 10.00) + (childTickets * 6.00);  //adult tickets$10 child tickets $6
	netBoxoffice = (grossBoxoffice * 0.20);  //theater keeps 20% of gross earning
	paidToDistributer = (grossBoxoffice - netBoxoffice);  //distributer gets 80% of the earnings

	cout << fixed << setprecision(2);
	cout << "REVENUE REPORT" << endl;
	cout << "==============" << endl;
	cout << "Movie Name: " << setw(23) << "\"" << movieName << "\"" << endl;
	cout << "Adult Tickets Sold: " << setw(29) << adultTickets << endl;
	cout << "Child Tickets Sold: " << setw(29) << childTickets << endl;
	cout << "Gross Box Office Profit: " << setw(17) << "$" << grossBoxoffice << endl;
	cout << "Net Box Office Profit: " << setw(20) << "$" << netBoxoffice << endl;
	cout << "Amount paid to distributer: " << setw(14) << "$" << paidToDistributer << endl;
	cout << "\n";
	system("pause");
}
