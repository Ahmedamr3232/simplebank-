🏦 C++ Banking Management System
This is a full-featured Banking Management System written in C++ with file-based storage. It supports multi-user login, role-based permissions, and banking operations like managing clients, transactions, and system users.

📂 Features
👤 Client Management
Add new clients

View client list

Find a client by account number

Edit client information

Delete client accounts (soft-delete)

💸 Transactions
Deposit money

Withdraw money with validation

View total balances of all clients

👮 User Management (Admin Panel)
Add new users with permission control

List users

Update users

Delete users (except for "admin")

Find users

Admin has full access by default

🔐 Authentication System
Login screen

User credential validation

Permissions system using bitwise flags

🗂️ File Structure
File	Purpose
main.cpp	Main logic for login and launching the application
clientdata.txt	Stores client account information
usersdata.txt	Stores user credentials and permissions

🛡️ Permissions
Permissions are stored as bitwise flags:

Permission	Flag Value
Show Clients	1
Add Clients	2
Delete Clients	4
Edit Clients	8
Find Clients	16
Transactions	32
Manage Users	64

Admin user has permission value -1, which means full access.

🛠️ How It Works
1. Startup
Initializes the admin account (admin / 1234) if it doesn't exist.

Starts the login screen.

2. After Login
Loads the main menu based on user permissions.

User can perform actions like add/search/edit/delete clients or users depending on access.

3. File Handling
Client/user data is stored and retrieved from .txt files.

Vectors are used to manipulate data in memory before writing back to files.

💻 Compilation & Running
🔧 Requirements
C++17 compatible compiler (e.g., g++, MSVC)

Console/terminal

🧪 Compile & Run (Linux/Mac)
bash
نسخ
تحرير
g++ -o bank main.cpp
./bank
🧪 Compile & Run (Windows, CMD)
cmd
نسخ
تحرير
g++ -o bank.exe main.cpp
bank.exe
📌 Notes
Ensure clientdata.txt and usersdata.txt exist in the same directory as the executable or they will be created automatically.

Admin is the only user that cannot be deleted.

system("cls") and system("pause") are used — consider replacing them if you are using another OS.

📷 Sample User Credentials
Username	Password	Permissions
admin	1234	Full access

