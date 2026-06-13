# Bank Management System (C)

A simple console-based Bank Management System written in C. It allows users to create, view, search, update, and delete bank accounts, along with deposit and withdrawal operations. All data is stored in a plain text file (`record.txt`), making it human-readable and easy to inspect.

## Features

- 🔐 **Password-protected login**
- ➕ **Create Account** – add a new account with name, age, address, phone, account type, and initial balance
- 📋 **View All Accounts** – display all records in a formatted table
- 🔍 **Search Account** – find an account by account number
- 💰 **Deposit Money** – add funds to an existing account
- 💸 **Withdraw Money** – withdraw funds with balance check
- ✏️ **Update Account** – edit address and phone number
- 🗑️ **Delete Account** – remove an account permanently
- 🎨 **Color-coded terminal output** (success, error, prompts, headers)

## Data Storage

Records are stored in `record.txt` as plain text, one record per line, using `|` as a field separator:

```
acc_no|name|age|address|phone|acc_type|balance
```

This makes the data file easy to view, edit, or back up using any text editor.

## Getting Started

### Prerequisites

- A C compiler (e.g., `gcc`)
- A terminal that supports ANSI color codes (Linux, macOS, WSL, or modern Windows Terminal)

### Build

```bash
gcc bank.c -o bank
```

### Run

```bash
./bank
```

### Default Login

```
Password: iamlearning
```

> ⚠️ For learning/demo purposes only — change the hardcoded password before any real-world use.

## Menu Options

```
1. Create Account
2. View All Accounts
3. Search Account
4. Deposit Money
5. Withdraw Money
6. Update Account
7. Delete Account
8. Exit
```

## Project Structure

```
.
├── bank_management.c   # Main source code
├── record.txt          # Auto-generated data file (created on first account creation)
└── README.md
```

## How It Works

- Each account is represented as a `struct Account` containing account number, name, age, address, phone, account type, and balance.
- Operations that modify existing records (deposit, withdraw, update, delete) read the entire file, apply changes, write to a temporary file, then replace the original — since text records have variable length.

## Future Improvements

- [ ] Encrypt or hash the login password
- [ ] Add transaction history logging
- [ ] Support multiple user roles (admin/customer)
- [ ] Input validation for edge cases

## License

This project is open-source and available for educational use.
