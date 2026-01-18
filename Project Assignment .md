PROJECT TITLE

Student Management System (SMS)

A simple Python program used to add, view, and delete student records.

SOFTWARE DEVELOPMENT LIFE CYCLE (SDLC)
1. Requirement Analysis

The goal of the project is to manage student records.

Functional Requirements

Add a student

View all students

Delete a student

Exit the system

Non-Functional Requirements

Easy to use

Runs on any system with Python installed

Data stored temporarily during execution

2. System Design

The system is designed as a menu-driven console application.

Main Components

students → dictionary to store student data

add_student() → adds a new student

view_students() → displays all students

delete_student() → removes a student

main() → controls program flow

📌 Note:
All function names used here are the same names used in the implementation, as required.

3. Implementation (Python Code)

Create a file named student_management_system.py

# Student Management System

students = {}

def add_student():
    student_id = input("Enter student ID: ")
    name = input("Enter student name: ")
    students[student_id] = name
    print("Student added successfully.\n")

def view_students():
    if not students:
        print("No students found.\n")
    else:
        print("Student Records:")
        for student_id, name in students.items():
            print(f"ID: {student_id}, Name: {name}")
        print()

def delete_student():
    student_id = input("Enter student ID to delete: ")
    if student_id in students:
        del students[student_id]
        print("Student deleted successfully.\n")
    else:
        print("Student not found.\n")

def main():
    while True:
        print("Student Management System")
        print("1. Add Student")
        print("2. View Students")
        print("3. Delete Student")
        print("4. Exit")

        choice = input("Choose an option: ")

        if choice == "1":
            add_student()
        elif choice == "2":
            view_students()
        elif choice == "3":
            delete_student()
        elif choice == "4":
            print("Exiting program...")
            break
        else:
            print("Invalid choice. Try again.\n")

main()

4. Testing

The system was tested by:

Adding multiple students

Viewing student records

Deleting existing and non-existing students

Checking invalid menu inputs

All functions worked as expected.

5. Deployment

The program can be deployed by:

Installing Python

Running the file using:

python student_management_system.py

6. Maintenance

Future improvements may include:

Saving data to a file or database

Editing student records

Adding user authentication

Creating a graphical interface
