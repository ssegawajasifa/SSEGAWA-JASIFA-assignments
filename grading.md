# Grading Multiple Choice Questions Program

## Overview
This program reads a set of answers for 8 students and compares them with the correct answer key for 10 questions. It then calculates how many questions each student answered correctly and displays the result.

## 1. OOP Concepts Used
This program is mainly written in a procedural style, not a full object-oriented style. It does not use classes, objects, inheritance, polymorphism, or encapsulation.

However, some basic programming principles are still present:
- Data organization: The answers are stored in a 2D array, which groups each student’s answers together.
- Structured data: The answer key is stored separately as a 1D array.
- Reusability: The code can be extended easily if more students or questions are added.

If this program were rewritten using OOP, we could create a Student class with:
- a member for the student’s answers
- a method to calculate the score
- a method to display the result

This would improve organization and make the program easier to maintain.

## 2. Algorithm and Main Steps
The program follows this simple algorithm:

1. Store all student answers in a 2D array called `answers`.
2. Store the correct answers in a 1D array called `key`.
3. Loop through each student using `for (int student = 0; student < 8; ++student)`.
4. For each student, set `correct = 0` to start counting correct answers.
5. Loop through each question using `for (int question = 0; question < 10; ++question)`.
6. Compare the student’s answer at `answers[student][question]` with the correct answer at `key[question]`.
7. If they match, increase the `correct` counter by 1.
8. After checking all questions, print the student’s score.
9. Repeat the process for all students.

This algorithm is efficient because it compares each answer once and does not require any complicated logic.

## 3. Possible Error Points
There are several potential issues to watch out for:

- Wrong array size: If the number of answers does not match the number of questions, the comparison may fail or produce incorrect results.
- Typing mistakes: A single incorrect character in the answer key or in a student’s answers can change the score.
- Case sensitivity: The program compares characters exactly. If a student enters lowercase letters instead of uppercase letters, the comparison may fail.
- Out-of-range errors: If the loops are changed incorrectly, it may try to access an array element that does not exist.
- Hard-coded values: Using `8` and `10` directly can be risky if the data size changes later. Using constants would make the code safer and easier to update.
- Wrong indexing: A mistake in the index values could compare the wrong answer with the wrong question.
- Data mismatch: If one student has a different number of answers than the others, the logic may produce incorrect scores.

## Conclusion
This program is a good example of using arrays to store exam data and compare answers automatically. It is simple, readable, and effective for grading multiple-choice questions. Although it does not use strong object-oriented concepts, it demonstrates clear data organization and logical comparison.
