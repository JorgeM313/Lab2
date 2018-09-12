# Lab2
//Author: Jorge Martinez
//CPSC 121 Lab 2
// 9/12/18
#include<iostream>

using namespace std;

int main()
{
  double Quiz_inp = 0;
  double Quiz = 0;
  double Lab_inp = 0;
  double Lab = 0;
  double Mid_inp = 0;
  double Mid = 0;
  double Final_inp = 0;
  double Final = 0;
  double Part_inp = 0;
  double Part = 0;
  double class_grade = 0;
  double poss_grade = 100;
  double avgtotal = 0;

  cout << "Please enter the average grade (as a percent out of 100) for each of the following grade categories: \n";
  cout << "Note: if there is no data for a category, please enter the value of -1 into that category. \n";
  cout << "This will exclude that particular category when calculating the class grade.\n";
  cout << "Quizzes: ";
  cin >> Quiz_inp;
  if (Quiz_inp == -1){
    Quiz = 0;
    poss_grade = poss_grade - 10;
  }
  cout << "Labwork: ";
  cin >> Lab_inp;
  if (Lab_inp == -1){
    Lab = 0;
    poss_grade = poss_grade - 35;
  }
  cout << "Midterm: ";
  cin >> Mid_inp;
  if (Mid_inp == -1){
    Mid = 0;
    poss_grade = poss_grade - 15;
  }
  cout << "Final: ";
  cin >> Final_inp;
  if (Final_inp == -1){
    Final = 0;
    poss_grade = poss_grade - 30;
  }
  cout << "Participation: ";
  cin >> Part_inp;
  if (Part_inp == -1){
    Part = 0;
    poss_grade = poss_grade - 10;
  }
  Quiz = Quiz_inp / 10;
  Lab = (Lab_inp * 35) / 100;
  Mid = (Mid_inp * 15) / 100;
  Final = (Final_inp * 3) / 10;
  Part = Part_inp / 10;
  avgtotal = Quiz + Lab + Mid + Final + Part;
  class_grade  = avgtotal / poss_grade * 100;
  cout << "Here are your results: \n";
  if (class_grade >= 90 && class_grade <= 100){
    cout << "Your grade in the class is " << class_grade << "percent. You have an A. \n";
  }
  else if (class_grade >= 80 && class_grade < 90){
    cout << "Your grade in the class is " << class_grade << "percent. You have a B. \n";
  }
  else if (class_grade >= 70 && class_grade < 80){
    cout << "Your grade in the class is " << class_grade << "percent. You have a C. \n";
  }
  else if (class_grade >= 60 && class_grade < 70){
    cout << "Your grade in the class is " << class_grade << "percent. You have a D. \n";
  }
  else if (class_grade >= 0 && class_grade < 60){
    cout << "Your grade in the class is " << class_grade << "percent. You have an F. \n";
  }
  return 0;
}
