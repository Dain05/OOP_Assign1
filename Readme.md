# Intro to Object Oriented Programming  
## Module 1 – Assignment 1  
### XYZ Bank ATM Program

*Course:* Introduction to Object Oriented Programming  
*Lecturer:* Doron Williams  
*Date:* November 1, 2025  

*Group Members*

- Dain Thorpe  
- Shanique Wisdom  
- Joan Johnson-Brown  
- Dante Graham  
- Pasha Pinnock  

---

## Description

This project is a simple C++ console application that simulates an ATM system for *XYZ Bank*.

Users can:

1. Check their account balance  
2. Deposit money  
3. Withdraw money  
4. Exit the program  

The menu keeps running in a *while loop* until the user chooses the exit option.

---

## Account Class

The program uses an Account class to represent a customer’s bank account, based on the UML diagram in the assignment:

- Private attribute  
  - balance: double  

- Constructor  
  - Account(double init_balance)  
    - Validates that the initial balance is *>= 1000.00*  
    - If not valid, sets balance to 0 and prints a warning message  

- Member functions  
  - double deposit(double amount)  
    - Adds amount to the current balance (if amount > 0)  
  - bool withdraw(double amount)  
    - Withdraws amount if there is enough balance  
    - If amount is greater than the balance, prints  
      "Debit amount exceeded account balance."  
  - double getBalance() const  
    - Returns the current account balance  

---

## Menu and Control Flow

- The main program asks the user for an *initial balance*, then creates an Account object.
- A *while loop* and *switch statement* are used to handle the menu options:
  - Option 1 – Display current balance  
  - Option 2 – Deposit money  
  - Option 3 – Withdraw money  
  - Option 4 – Exit the program  
- Invalid menu choices are handled with an error message.

---

## How to Compile and Run (MSYS2 / g++)

From the folder that contains main.cpp:

```bash
g++ -std=c++20 -Wall main.cpp -o atm.exe
./atm.exe