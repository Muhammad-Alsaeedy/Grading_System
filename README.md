# Student Grade Management System

A simple console program written in Python that accepts student marks, calculates the average mark and letter grade, validates all input, and displays the results.

This project was built as part of a **Personal Software Process (PSP)** assignment. The work was estimated, timed and logged using a Job Number Log and a Daily Time Log.

## Features

- Accepts a student name or ID (cannot be empty)
- Accepts marks for **7 subjects** per student
- Validates every mark: it must be a number between **0 and 100**, and the program asks again if the input is invalid
- Calculates the **average mark**
- Assigns a **letter grade** from the grading scale below
- Supports **multiple students** in one run
- Displays the name, marks, average (2 decimal places) and grade of every student at the end

## Grading Scale

| Average mark | Grade |
|--------------|-------|
| 95 and above | A+ |
| 85 to below 95 | A |
| 80 to below 85 | A- |
| 75 to below 80 | B+ |
| 70 to below 75 | B |
| 65 to below 70 | B- |
| 60 to below 65 | C+ |
| 50 to below 60 | C |
| 40 to below 50 | D |
| Below 40 | F |

## Requirements

- Python 3.6 or newer (uses f-strings)
- No external libraries

## How to Run

```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
python grade_system.py
```

On some systems use `python3 grade_system.py`.

## Example Session

```
Enter student name or ID: Abel
  Mark for subject 1 (0-100): 80
  Mark for subject 2 (0-100): 90
  Mark for subject 3 (0-100): 70
  Mark for subject 4 (0-100): 60
  Mark for subject 5 (0-100): 100
  Mark for subject 6 (0-100): 50
  Mark for subject 7 (0-100): 75
Add another student? (y/n): n

===== RESULTS =====
Name:    Abel
Marks:   80, 90, 70, 60, 100, 50, 75
Average: 75.00
Grade:   B+
----------------------------------------
```

## Input Validation

| Input | Result |
|-------|--------|
| Empty name | "Name cannot be empty. Try again." |
| Text instead of a number (for example `abc`) | "Invalid input: please enter a number." |
| Mark below 0 or above 100 | "Invalid input: mark must be between 0 and 100." |

## Code Structure

| Function | Purpose |
|----------|---------|
| `get_letter_grade(average)` | Returns the letter grade for an average mark |
| `calculate_average(marks)` | Returns the average of a list of marks |
| `get_student_name()` | Asks for a name or ID until a non-empty value is entered |
| `get_valid_mark(subject_number)` | Asks for one mark until it is valid |
| `read_student()` | Collects one student's data and returns it as a dictionary |
| `display_student(student)` | Prints one student's record |
| `main()` | Runs the input loop and shows all results |

Settings such as `NUM_SUBJECTS`, `MIN_MARK`, `MAX_MARK` and `GRADE_SCALE` are defined at the top of `grade_system.py` and can be changed easily.

## PSP Jobs

The project was split into five jobs, each estimated before starting and logged after finishing:

1. Requirements analysis
2. Design
3. Implementation
4. Testing
5. Documentation