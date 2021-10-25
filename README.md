# Lecture8

  #include <iostream>
  #include <string>
  using namespace std;

  void dateofthemonth(void);
  void temperatur(void);
  void grade(void);
  void fuelmeup(void);

  int main() {

	int ichoice=0;
	cout << "Lecture 8!" << endl;
	cout << "Choose 1 to 4\n" << endl;
	cout << " 1 = dateofthemonth\n 2 = temperature\n 3 = gradechecker\n 4 = fuel me up" << endl;
	cin >> ichoice;
	
	while (cin.fail()) {
		cout << "Invalid! please Try again!" << endl;
		cin.clear();
		cin.ignore(1000, '\n');
		cin >> ichoice;
	}
//Dateofthemonth
	if (ichoice == 1) {
		dateofthemonth();
		cout << endl;
	}
//Temperature
	else if (ichoice == 2) {
		temperatur();
		cout << endl;
	}
//GradeChecker
	else if (ichoice == 3) {
		grade();
		cout << endl;
	}
//Fuelmeup
	else if (ichoice == 4) {
		fuelmeup();
		cout << endl;
	}
	else {
		cout << "Invalid number!" << endl;
	}
	return 0;
  }

//Date of the month
  void dateofthemonth(void) {
	int inum;
	cout << "Days of the month!" << endl;
	cout << "Type the month: " << endl;
	cout << " 1: January\n"
		<< " 2: Febuary\n"
		<< " 3: March\n"
		<< " 4: April\n"
		<< " 5: May\n"
		<< " 6: June\n"
		<< " 7: July\n"
		<< " 8: August\n"
		<< " 9: September\n"
		<< " 10: October\n"
		<< " 11: November\n"
		<< " 12: December\n";
	cin >> inum;

	switch (inum) {
	case 1:
		cout << "January have 31 days" << endl;
		break;
	case 2:
		cout << "Febuary have 28 days\n29 days after 3 years " << endl;
		break;
	case 3:
		cout << "March have 31 days;" << endl;
		break;
	case 4:
		cout << "April have 30 days " << endl;
	case 5:
		cout << "May have 31 days " << endl;
		break;
	case 6:
		cout << "June have 30 days " << endl;
		break;
	case 7:
		cout << "July have 31 days " << endl;
		break;
	case 8:
		cout << "August have 31 days " << endl;
		break;
	case 9:
		cout << "September have 30 days" << endl;
		break;
	case 10:
		cout << "October have 31 days " << endl;
		break;
	case 11:
		cout << "November have 31 days " << endl;
		break;
	case 12:
		cout << "December have 31 days " << endl;
		break;
	default:
		cout << "Invalid!" << endl;
		break;
	}
  }

  //Temperaturechecker
  void temperatur(void) {

	double num;
	char temp = 0;
	cout << "Temperature switch!" << endl;
	cout << " Celcius to Farenheit/ Farenheit to Celcius" << endl;
	cout << "Type 'c' or 'f'" << endl;
	cin >> temp;

	switch (temp) {
		{
	case 'c':
	case 'C':
		cout << "Type the Celcius to convert to Farenheit!" << endl;
		cin >> num;

		cout << (num * 9 / 5) + 32 << " Farenheit!" << endl;
		break;
		}
		{
	case 'f':
	case 'F':
		cout << "Type the Farenheit to conver to Celcius!" << endl;
		cin >> num;

		cout << (num - 32) * 5 / 9 << " Celcius" << endl;
		break;
		}

	default:
		cout << "Invalid input!" << endl;
	}
  }

  //Gradechecker
  void grade(void) {

	char options;
	string name;
	char igrade;
	cout << "Grade Checker! " << endl;
	cout << "Type your name: " << endl;
	cin >> name;

	cout << "Okay, " << name << "Do you want to know your grade?" << endl;
	cout << " (Y/N)" << endl;
	cin >> options;

	switch (options) {
	case 'n':
	case 'N':
		cout << "Okay, Goodbye " << name << endl;
		break;
	case 'y':
	case 'Y':
	cout << "Type your grade! " << endl;
	cout << "Type your grade A-F" << endl;
	cin >> igrade;
	// A = 70 - 100
	// B = 69 - 60
	// c = 59 - 50
	// d = 49 - 40
	// F = 39 below

	switch (igrade) {
		{
	case 'a':
	case 'A':
		cout << "70 - 100 \nCongratulation!" << endl;
		break;
		} {
	case 'b':
	case 'B':
		cout << "69 - 60 \nGreat job!" << endl;
		break;
		} {
	case 'c':
	case 'C':
		cout << "59 - 50 \nGood job! You can do this!" << endl;
		break;
		} {
	case 'D':
	case 'd':
		cout << "49 - 40 \nNice try! I know you can do this!" << endl;
		break;
		} {
	case 'F':
	case 'f':
		cout << "39 below! \nIts okay! You can do it next time!" << endl;
		break;
		}
	}
	default:
		cout << "Invalid " << endl;
		break;
	}
  }

  void fuelmeup(void) {

	char gas;
	double dnum;
	cout << "Fuel me up!" << endl;
	cout << "What fuel do you need? Petrol or Diesel?" << endl;
	cout << "P or D" << endl;
	cin >> gas;

	switch (gas) {
	case 'P':
	case 'p':
		cout << "Petrol? How much?" << endl;
		cin >> dnum;

		cout << "Petrol here for " << (dnum * 2.42) << " AED" << endl;
		break;
	case 'd':
	case 'D':
		cout << "Diesel? How much?" << endl;
		cin >> dnum;

		cout << "Diesel here for " << (dnum * 2.51) << " AED" << endl;
		break;
	default:
		cout << "Invalid" << endl;
		break;
	}
}
