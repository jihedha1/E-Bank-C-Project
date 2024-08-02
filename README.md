# Bank Management System

This is a simple console-based Bank Management System implemented in C. The system allows for the management of clients and accounts, as well as conducting basic transactions such as withdrawals, deposits, and fund transfers between accounts.

## Features

### Client Management
- Add a client
- Modify client information
- Delete a client
- List all clients

### Account Management
- Add an account
- Search for an account
- List all accounts
- Delete an account
- Close an account

### Transaction Management
- Withdraw money
- Deposit money

### Additional Features
- Transfer funds between accounts

## File Structure

- `main.c`: The main program file containing the menu and all functionalities.
- `clients.dat`: A binary file that stores client information.
- `accounts.dat`: A binary file that stores account information.
- `temp.dat`: A temporary binary file used for modifying and deleting records.
## Functions

### Main Functions

- `int menu()`: Displays the main menu and handles user input.
- `void manageClients()`: Manages client-related operations.
- `void manageAccounts()`: Manages account-related operations.
- `void manageTransactions()`: Manages transaction-related operations.
- `void transferFunds()`: Handles fund transfers between accounts.

### Client Management Functions

- `void addClient()`: Adds a new client.
- `void modifyClient()`: Modifies existing client information.
- `void deleteClient()`: Deletes a client.
- `void showClients()`: Lists all clients.

### Account Management Functions

- `void addAccount()`: Adds a new account.
- `void searchAccount()`: Searches for an account by ID.
- `void showAllAccounts()`: Lists all accounts.
- `void deleteAccount()`: Deletes an account.
- `void closeAccount()`: Closes an account.

### Transaction Management Functions

- `void withdraw()`: Withdraws money from an account.
- `void deposit()`: Deposits money into an account.

### Utility Functions

- `int compareClients(const void* a, const void* b)`: Compares two clients by last name.

## Data Structures

### Client Structure

```c
typedef struct {
    int id;
    char lastName[10];
    char firstName[10];
} Client;

Account Structure

c

typedef struct {
    int id;
    int clientId;
    int balance;
    int day;
    int month;
    int year;
} Account;

## Compilation and Execution

To compile and run the program, use the following commands:

```bash
gcc -o bank_management main.c
./bank_management
