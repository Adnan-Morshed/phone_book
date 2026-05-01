# 📚 Phonebook Management System

> *Your Digital Contacts Companion* ✨

A sleek command-line phonebook application written in **C** that allows users to manage contact information with essential CRUD (Create, Read, Update, Delete) operations. Perfect for learning file I/O and data structure management!

## ✨ Features

- 🆕 **Add New Contact**: Store contact details including name, address, email, and phone number
- 👀 **View All Contacts**: Display all saved contacts in the phonebook
- 🔍 **Search Contacts**: Search for contacts by name (substring matching supported)
- ✏️ **Modify Contacts**: Update existing contact information
- 🗑️ **Delete Contacts**: Remove contacts from the phonebook
- 💾 **Persistent Storage**: All contacts are saved to a binary file (`PHONEBOOK.PHN`)

## 🚀 Getting Started

### 📋 Prerequisites

- 🖥️ **GCC** or any C compiler (e.g., MinGW on Windows, GCC on Linux/Mac)
- 📦 Standard C libraries

### ⚙️ Compilation

Compile the program using any C compiler:

```bash
gcc phonebook.c -o phonebook
```

### ▶️ Running the Program

Execute the compiled program:

```bash
./phonebook
```

Or on Windows:

```bash
phonebook.exe
```

## 📖 Usage

The program presents an interactive menu with the following options:

```
╔═══════════════════════════════════════════════╗
║    📱 PHONEBOOK MANAGEMENT SYSTEM 📱         ║
╠═══════════════════════════════════════════════╣
║  1️⃣  ADD NEW CONTACT                         ║
║  2️⃣  VIEW ALL CONTACTS                       ║
║  3️⃣  SEARCH CONTACTS                         ║
║  4️⃣  MODIFY CONTACTS                         ║
║  5️⃣  DELETE CONTACT                          ║
║  6️⃣  EXIT                                    ║
╚═══════════════════════════════════════════════╝
```

### 📝 Main Operations

#### 1️⃣ Add New Contact
- Select option `1` from the main menu
- Enter contact details: **Name**, **Address**, **Email**, and **Phone Number**
- Option to add multiple contacts in succession
- Returns to main menu after completion

#### 2️⃣ View All Contacts
- Select option `2` from the main menu
- Displays all saved contacts with complete information
- Shows message if no contacts exist

#### 3️⃣ Search Contacts
- Select option `3` from the main menu
- Enter search text *(case-insensitive)* 🔤
- Displays all contacts matching the search term
- Supports substring matching (e.g., searching "john" will find "John Smith")

#### 4️⃣ Modify Contacts
- Select option `4` from the main menu
- Enter the exact name of the contact to modify
- Re-enter all contact details
- Updates the contact in the phonebook

#### 5️⃣ Delete Contact
- Select option `5` from the main menu
- Enter the exact name of the contact to delete
- Contact is permanently removed from the phonebook

#### 6️⃣ Exit
- Select option `6` to close the application

## 🗂️ File Structure

```
📦 phonebook/
 ├── 📄 phonebook.c              # Main source code
 ├── 💾 PHONEBOOK.PHN            # Binary data file (auto-created)
 └── 📖 README.md               # This file
```

## 📊 Data Storage

- 💿 All contacts are stored in a **binary file** named `PHONEBOOK.PHN`
- 🔄 The file is automatically created when the program runs for the first time
- 🔒 Data persists between program executions

## 👤 Contact Structure

Each contact contains:
- **👤 Name**: Up to 100 characters
- **🏠 Address**: Up to 200 characters  
- **📧 Email**: Up to 100 characters
- **☎️ Phone Number**: Integer value

## 🏗️ Technical Details

### 🎯 Architecture
- 🖱️ Command-line interface with menu-driven navigation
- 📂 File-based storage using binary serialization
- 🔤 Case-insensitive search functionality
- 📋 Temporary file handling for delete operations

### 🔧 Key Functions

| Function | Purpose | Icon |
|----------|---------|------|
| `mainMenu()` | Displays main menu and handles user selection | 🏠 |
| `addContact()` | Adds new contacts to the phonebook | ➕ |
| `readContacts()` | Displays all saved contacts | 👁️ |
| `searchContact()` | Searches for contacts by name | 🔍 |
| `modifyContact()` | Updates existing contact information | ✏️ |
| `deleteContact()` | Removes contacts from the phonebook | 🗑️ |
| `basicDetails()` | Collects contact information from user | 📝 |
| `checkForMatch()` | Helper function for substring matching | 🎯 |
| `menuDesign()` | Displays formatted menu headers | 🎨 |

## ⚠️ Limitations

- 🔍 Search is limited to the name field
- 🎯 Contact names must be unique for modify/delete operations
- 📞 No input validation for phone numbers (accepts any integer)
- 👥 No support for multiple contacts with the same name
- 🪟 Requires Windows/DOS environment for `conio.h` library (system() calls)

## 🚀 Future Improvements

- ✅ Add input validation for email and phone number formats
- 📊 Implement sorting options (by name, phone number, etc.)
- 📤 Add export functionality (CSV, TXT)
- 🎨 Support for editing individual fields rather than all fields at once
- 🔎 Add duplicate contact detection
- 📁 Implement contact categories or groups
- 💾 Add backup and restore functionality
- 🌍 Cross-platform compatibility improvements
- 🔐 Add password protection for sensitive data
- 📱 Mobile app version in future

## 🛠️ Compilation Issues Fixed

The original code had several compilation errors that have been resolved:

| Issue | Solution |
|-------|----------|
| 🔴 Duplicate includes | Removed duplicate `#include<stdio.h>` |
| 🟠 Structure definition | Changed from `struct PhoneBook` to `typedef struct` for cleaner usage |
| 🟡 Main function | Added proper return type `int` and return statement |
| 🟢 Code formatting | Improved readability with proper spacing and indentation |
| 🔵 Function declarations | Organized and cleaned up all function prototypes |
| 🟣 File operations | Added proper file pointer handling and closing |
| ⚫ Memory safety | Fixed buffer overflow potential in `checkForMatch()` function |

## 📜 License

This project is provided as-is for educational purposes. 📚

## 🤝 Contributing

Feel free to fork this project and submit pull requests for any improvements! 🌟

We welcome:
- 🐛 Bug reports
- 💡 Feature suggestions
- 🧹 Code improvements
- 📝 Documentation enhancements

## 👨‍💻 Author

Created as a **C programming learning project** | *Made with ❤️*

---

> **Note**: 🪟 This application uses DOS/Windows-specific functions (`conio.h`, `system("cls")`). For cross-platform compatibility, these should be replaced with standard C alternatives or platform-specific equivalents.

---

<div align="center">

### ⭐ If you found this helpful, please give it a star! ⭐

**Happy Coding!** 💻✨

</div>
