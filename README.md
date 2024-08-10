# Task-1
  #include <iostream>
#include <cstdlib>
#include <fstream>
using namespace std;

int main()
{
    ofstream out("GuessMyNumber.out");

    int num, guess, tries = 0;

    num = rand() % 100 + 1;
    
    cout << "Guess My Number Game\n\n";
     out << "Guess My Number Game\n\n";

    do
    {
        cout << "\nEnter a GUESS between 1 and 100:\n";
         cin >> guess;
         out << guess;
         tries++;

        if(guess > num)
          {
            cout << "Your GUESS is TOO HIGH, try again!\n";
             out << "Your GUESS is TOO HIGH, try again!\n";
          }
        else if(guess < num)
          {
            cout << "Your GUESS is TOO LOW, try again!\n";
             out << "Your GUESS is TOO LOW, try again!\n";
          }
        else
          {
            cout << "\nCorrect! It only took " << tries << " guesses!\n";
             out << "\nCorrect! It only took " << tries << " guesses!\n";
          }
    }
    while(guess != num);

    out.close();
    return 0;
}
