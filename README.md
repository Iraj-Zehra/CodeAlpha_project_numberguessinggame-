#include <iostream>
#include <cstdlib>
#include <ctime>   

using namespace std;

int main()
 {
    srand(static_cast<unsigned>(time(0))); 
    int numberToGuess = rand() % 100 + 1; 
    int playerGuess = 0;                  
    int attempts = 0; 
    cout << "Welcome to the Number Guessing Game!" << endl;
    cout << "I have chosen a number between 1 and 100." << endl;
    cout << "Your task is to guess the number. Let's begin!" << endl;
    do {
        cout << "Enter your guess: ";
        cin >> playerGuess;
        attempts++; 
        if (playerGuess > numberToGuess) 
        {
            cout << "Your guess is too high. Try again!" << endl;
        } 
        else if (playerGuess < numberToGuess) 
        {
            cout << "Your guess is too low. Try again!" << endl;
        }
         else 
         {
            cout << "Congratulations! You guessed the number in " << attempts << " attempts!" << endl;
        }
    } 
    while (playerGuess != numberToGuess); 
    cout << "Thanks for playing! Goodbye!" << endl;

    return 0;
}
