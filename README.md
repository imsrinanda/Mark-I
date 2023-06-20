# Attendance Tracking System

This documentation provides an overview and instructions for a Python mini project that involves tracking attendance of students. The project includes functionalities such as importing attendance data from CSV files, generating an Excel sheet with consolidated attendance, checking attendance details of a specific student, calculating attendance percentage, determining eligibility for writing exams, marking attendance, and checking the number of classes a student can miss.

## Table of Contents
- [Introduction](#introduction)
- [Functionality](#functionality)
- [User-Defined Functions](#user-defined-functions)
- [Running the Project](#running-the-project)
- [Outputs](#Outputs)

## Introduction
The Python mini project is designed to manage attendance records of students. It utilizes CSV files containing attendance data and provides various functions to analyze and manipulate the attendance information.

## Functionality
The project offers the following functionalities:

1. Importing Attendance Data: CSV files containing attendance data are imported using the `pandas` library and concatenated to create a consolidated attendance dataframe.

2. Consolidating Attendance: The consolidated attendance dataframe is saved as an Excel file named "attendance.xlsx".

3. Checking Attendance Details: The `check` function allows users to view the attendance details of a specific student. It provides options to retrieve attendance based on a specific date, a range of dates, or every day in a month.

4. Calculating Attendance Percentage: The `check_attendance_percentage` function calculates the attendance percentage of a particular student based on their roll number. It displays the total classes attended, total classes missed, leave classes, and attendance percentage.

5. Determining Exam Eligibility: The `eligibility` function determines whether a student is eligible to write the final examination based on their attendance percentage. If the attendance percentage is 85% or higher, the student is considered eligible.

6. Marking Attendance: The `mark_attendance` function allows users to mark the attendance of a student. It prompts for the student's name, roll number, subject, date, and presence status (present or absent). It then updates the attendance records accordingly.

7. Checking Missable Classes: The `missable_class` function calculates the number of classes a student can miss based on their current attendance percentage.

## User-Defined Functions

### check(attendance, roll_number)
This function prints the attendance of a specific student based on the provided roll number. It prompts the user to choose an option for retrieving attendance: specific date, range of dates, or every day in the month.

**Syntax:**
```python
check(attendance, roll_number)
```

### check_attendance_percentage(roll_number)
This function calculates the attendance percentage of a particular student based on the provided roll number. It displays the total classes attended, total classes missed, leave classes, and attendance percentage.

**Syntax:**
```python
check_attendance_percentage(roll_number)
```

### eligibility(roll_number)
This function determines if a student is eligible to write the final examination based on the provided roll number. It checks the student's attendance percentage and prints a corresponding message.

**Syntax:**
```python
eligibility(roll_number)
```

### missable_class(roll_number)
This function calculates the number of classes a student can miss based on the provided roll number and current attendance percentage.

**Syntax:**
```python
missable_class(roll_number)
```

### mark_attendance(name, roll_no, subject, date, is_present)
This function marks the attendance of a student. It prompts for the student's name, roll number, subject, date, and presence status (present or absent). The attendance records are then updated accordingly.

**Syntax:**
```python
mark_attendance(name, roll_no, subject, date, is_present)
```

## Running the Project
To run the

 project, follow these steps:

1. Import the necessary libraries:
```python
import pandas as pd
```

2. Import the attendance data from CSV files using the `pd.read_csv()` function:
```python
att1 = pd.read_csv("/content/201 att.csv")
att2 = pd.read_csv("/content/202 att.csv")
att3 = pd.read_csv("/content/203 att.csv")
att4 = pd.read_csv("/content/204 attendance.csv")
att5 = pd.read_csv("/content/205 attendance.csv")
att6 = pd.read_csv("/content/206 attendance.csv")
```

3. Concatenate the attendance dataframes using `pd.concat()`:
```python
attendance = pd.concat([att1, att2, att3, att4, att5, att6])
```

4. Save the consolidated attendance dataframe as an Excel file using `attendance.to_excel()`:
```python
file_name = 'attendance.xlsx'
attendance.to_excel(file_name)
print('DataFrame is written to Excel File successfully.')
```

5. Utilize the provided user-defined functions to interact with the attendance data:
- To check attendance details of a specific student, use the `check()` function:
```python
check(attendance, roll_number)
```

- To calculate the attendance percentage of a particular student, use the `check_attendance_percentage()` function:
```python
check_attendance_percentage(roll_number)
```

- To determine exam eligibility of a student, use the `eligibility()` function:
```python
eligibility(roll_number)
```

- To mark the attendance of a student, use the `mark_attendance()` function:
```python
mark_attendance(name, roll_no, subject, date, is_present)
```

- To check the number of classes a student can miss, use the `missable_class()` function:
```python
missable_class(roll_number)
```

6. Run the project within a loop to perform multiple operations by taking user input:
```python
op1 = input("No. of times you want to run the program? ")
op1 = int(op1)

for i in range(op1):
    op2 = input('''
    Welcome to Attendance Tracking System!
    ...
    ''')
    op2 = int(op2)
    if op2 == 1:
        roll_number = input("Enter the Roll no. of the student: ")
        check(attendance, roll_number)
    elif op2 == 2:
        roll_number = input("Enter the Roll no. of the student you want to check: ")
        check_attendance_percentage(roll_number)
    ...
```
## Outputs
### 1 Viewing the attendance details of a specific student:
![image](https://github.com/imsrinanda/Mark-I/assets/118894828/707bb263-b84e-44e0-bf28-cd583e3971db)
### 2 Checking attendance percentage:
![image](https://github.com/imsrinanda/Mark-I/assets/118894828/b09d26b3-8d94-4b87-b42d-28cea007937f)
### 3 Checking if a particular student is eligibe to write the exams:
![image](https://github.com/imsrinanda/Mark-I/assets/118894828/fcb5508b-4f03-4313-aa99-dbd71c9348fd)
### 4 Marking the attendance:
![image](https://github.com/imsrinanda/Mark-I/assets/118894828/5f3d25e8-298e-42e4-a166-02c4a41dc5d4)
### 5 Checking the classes the student can miss:
![image](https://github.com/imsrinanda/Mark-I/assets/118894828/7e29489c-6235-4c2d-9d25-673bfbf202c5)
### 6 Exit:
There isn't any special output, however the program stops running when this option is chosen.





