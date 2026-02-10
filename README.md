# Digital Attendance System for Hour-Based Lectures

Console-based C++ capstone project for **EEE227** (HND Electrical Engineering, Level 200).

## Project Objective
This application digitizes attendance management for hour-based lectures to reduce paper-based errors and support reliable reporting.

## Features Implemented

### 1) Student Management
- Register students
- View all registered students
- Search students by index number

### 2) Attendance Session Management
- Create a lecture session with:
  - Course code
  - Date
  - Start time
  - Duration (minutes)
- Mark attendance as:
  - Present
  - Absent
  - Late
- Update attendance records

### 3) Reports and Summary
- Display attendance list for any session
- Display attendance summary counts (Present, Absent, Late)

### 4) File Persistence (Offline First)
- Saves students to `students.txt`
- Saves sessions to `session_<COURSE>_<DATE>.txt`
- Tracks session files in `sessions_index.txt`
- Automatically loads saved data when program starts

## Suggested Repository Structure

```text
digital-attendance-system/
│── main.cpp
│── README.md
│── students.txt
│── sessions_index.txt
│── session_EE201_YYYY_MM_DD.txt
```

## Build and Run (VS Code / g++)

```bash
g++ -std=c++17 -Wall -Wextra -pedantic -o attendance main.cpp
./attendance
```

## Weekly Implementation Mapping

### Week 1
- Initial project structure
- `Student` class (implemented as struct with clear fields)
- Add/view/search student functions

### Week 2
- `AttendanceSession` class (implemented as struct)
- Create lecture sessions
- Complete menu-driven program flow

### Week 3
- Attendance marking logic
- Session reports and summary
- Input validation improvements (numeric range checks, date/time/status validation)

### Week 4
- Save/load student and session data via text files (`fstream`)
- Refactoring and readability updates (modular functions)
- Final testing and documentation

## Data File Format

### students.txt
Each line:

```text
indexNumber|fullName|programme
```

### session file
Example: `session_EEE227_2026_02_24.txt`

```text
EEE227
2026-02-24
09:00
120
INDEX001|Present
INDEX002|Late
INDEX003|Absent
```

## Notes
- Program is designed for offline use on Windows-compatible console environments.
- All core operations are available through the main menu.
- Data is auto-saved when exiting and can also be saved manually.
