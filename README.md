# Backend-Java-Development
Airtribe - Backend Java Development - Assignment 1 

# Library Management System

## Overview
The **Library Management System** is a software project designed to manage a multi-branch library system. It allows libraries to manage books, patrons, librarians, and various operations such as book lending, returns, book transfers between branches, and patron management. The project is developed in **Java** using **Object-Oriented Programming (OOP)** principles.

## Features
- **Multi-Branch Library Support**: Manage multiple library branches with unique inventories.
- **Patron Management**: Add, update, and manage patrons across different library branches.
- **Book Management**: Handle book lending, returns, and renewals. Track borrowed and available books.
- **Book Search**: Search books by title or author across branches.
- **Book Transfer**: Move books between branches seamlessly.
- **Librarian Functions**: Librarians can issue, return, renew books, and manage patrons.
- **Inventory Tracking**: Maintain and manage books in the inventory of each branch.
- **Borrowing History**: Track books patrons have borrowed, including their borrowing history.

## Technologies
- **Java**: Core programming language.
- **OOP Principles**: Encapsulation, inheritance, and polymorphism are used throughout the project.
- **UML Diagrams**: The project includes class diagrams to visualize the system architecture.

## Project Structure
```
src
├── org.Assignment.Book
│   ├── Book.java
│   ├── BookInstance.java
│   └── BookStatus.java
├── org.Assignment.LibraryManagement
│   ├── Library.java
│   ├── LibraryInventory.java
│   └── MultibranchLibrarySystem.java
├── org.Assignment.UserManagement
│   ├── Accounts
│   │   ├── Author.java
│   │   ├── Librarian.java
│   │   └── Patron.java
│   └── Authentication.java
└── org.Assignment.Main
    └── LibraryManagementSystem.java
```

## Key Classes
1. **Library**:
   - Handles book lending, returns, renewals, and book searches.
   - Contains attributes like `libraryId`, `libraryName`, `libraryLocation`, `LibraryInventory`, and `Librarian`.
   
2. **LibraryInventory**:
   - Manages books in a specific branch. 
   - Supports adding, removing, and searching for books.

3. **MultibranchLibrarySystem**:
   - Manages multiple branches and facilitates transferring books between them.

4. **Patron**:
   - Represents a library user, storing information like name, ID, email, and borrowed books.

5. **Librarian**:
   - Manages library operations such as issuing, returning, and renewing books.
   - Handles adding and updating patron details.

6. **Book & BookInstance**:
   - **Book** contains metadata such as title, author, and ISBN.
   - **BookInstance** represents a specific copy of a book that can be borrowed or transferred.

## Installation and Setup
1. Clone this repository to your local machine:
    ```bash
    git clone https://github.com/your-repo/LibraryManagementSystem.git
    ```

2. Open the project in your favorite IDE (e.g., **IntelliJ IDEA**, **Eclipse**).
   
3. Ensure you have **Java JDK 8 or above** installed.

4. Run the `LibraryManagementSystem.java` class from the `org.Assignment.Main` package.

## How to Use
1. **Create Libraries**: Initialize libraries with a librarian and inventory.
2. **Manage Books**: Add books to the inventory of a branch.
3. **Add Patrons**: Librarians can add new patrons to the system.
4. **Lend/Return Books**: Patrons can borrow and return books through the system.
5. **Transfer Books**: Move books between branches using the `MultibranchLibrarySystem`.
6. **Search Books**: Search for books by title or author.
7. **Update Patron Info**: Librarians can update patron details such as email.

## Example Usage

```java
// Create a librarian
Librarian librarian = new Librarian("Alice Johnson", "LIB001", "alice.johnson@example.com", "L001");

// Create a library
Library library = new Library("L001", "Downtown Library", "Downtown", inventory, librarian);

// Add a new patron
Patron patron = librarian.addPatron("Bob Smith", "PAT001", "bob.smith@example.com");

// Issue a book
library.issueBook(bookInstance, patron);

// Return a book
library.returnBook(bookInstance, patron);

// Transfer a book between branches
multiBranchLibrarySystem.transferBooks("L001", "L002", "B1");

// Search books
List<BookInstance> foundBooks = library.searchBook("1984");
```

## UML Class Diagram
![LMS](https://github.com/user-attachments/assets/8a72ffab-28e2-4681-8313-1901d8b99d7b)


## Future Enhancements
- **Reservation System**: Allow patrons to reserve books.
- **Recommendation System**: Provide book recommendations to patrons based on their borrowing history.
- **Fine Calculation**: Implement fine handling for late returns.

