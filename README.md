# CGPA-calculator-
#include <iostream>
using namespace std;

int main() {
    int numSubjects;
    float grade, total = 0.0, cgpa;

    // Ask the user for the number of subjects
    cout << "Enter the number of subjects: ";
    cin >> numSubjects;

    // Loop to take grades for each subject
    for (int i = 1; i <= numSubjects; ++i) {
        cout << "Enter grade for subject " << i << " (on scale 4.0): ";
        cin >> grade;

        // Check for valid grade input (0.0 to 4.0)
        if (grade < 0.0 || grade > 4.0) {
            cout << "Invalid grade. Please enter a grade between 0.0 and 4.0." << endl;
            --i; // Stay on the same subject until valid input
        } else {
            total += grade;
        }
    }

    // Calculate CGPA
    cgpa = total / numSubjects;

    // Output the CGPA
    cout << "Your CGPA is: " << cgpa << endl;

    return 0;
}

