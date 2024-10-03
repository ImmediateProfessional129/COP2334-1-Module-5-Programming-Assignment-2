# COP2334-1-Module-5-Programming-Assignment-2
This is a repository link of the COP2334-1 Module 5 Programming Assignment 2.

// This program is designed to calculate how many floors are there, how many rooms are occupied, and how many are unoccupied in a hotel to figure out the occupancy rate.

// Include the header file.
#include <iostream>
using namespace std;
// Start the main function.
int main() {
  // Declare the variables.
  int floors, rooms = 0, occupied = 0;
  cout << "How many floors does the hotel have? ";
  cin >> floors;
  // Start the for loop.
  for (int i = 1; i <= floors; i++) {
    int roomsOnFloor, occupiedOnFloor;
    // Start the if statement.
    cout << "How many rooms are on floor " << i << "? ";
    cin >> roomsOnFloor;
    // Start the while loop.
    cout << "How many of those rooms are occupied? ";
    cin >> occupiedOnFloor;
    occupied += occupiedOnFloor;
    rooms += roomsOnFloor;
    cout << "How many of those rooms are unoccupied? ";
    cin >> roomsOnFloor;
    rooms -= roomsOnFloor;
  }
  // Display the results.
  cout << "The hotel has " << rooms << " rooms, " << occupied << " of which are occupied." << endl;
  cout << "The occupancy rate is " << (double)occupied / rooms * 100 << "%." << endl;
  return 0;
}

