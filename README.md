 Lab 9: Student Academic Record Viewer & File Handling

This repository contains the Python implementations for **Lab 9: File Handling**, demonstrating basic and advanced file manipulation, dynamic CSV parsing, data filtering using `pandas`, and dual user interface options (CLI for Google Colab & Desktop GUI via Tkinter).



Repository Contents

* **`Lab9_File_Handling.ipynb`**: The primary Google Colab notebook containing code blocks for file operations, interactive CSV uploads, and student grade searching.
* **`course_lists.csv`**: Sample structured dataset containing student records, course codes, course titles, academic units, instructors, and assigned grades.
* **`README.md`**: Project documentation and usage guide.


Features & Implementations

1. File Handling & CSV Data Parsing
* **Standard File Operations**: Demonstrates built-in Python file modes (`'w'`, `'r'`, `'a'`) for file creation, reading, writing, and appending.
* **Dynamic Header & Record Parsing**: Handles multi-student datasets with grouped course structures using `pandas` forward-fill (`ffill()`) logic to associate courses with their respective student names seamlessly.

2. Version 1: Console / Interactive CLI (Google Colab)
* Integrated with Google Colab's file upload API (`google.colab.files.upload()`).
* Dynamic student name detection from uploaded CSV files.
* Search and filter capability (case-insensitive partial matching) to display specific student grade reports cleanly in the terminal output.

3. Version 2: Desktop Graphical User Interface (GUI)
* Built using Python's standard `tkinter` and `ttk` desktop interface libraries.
* Native File Dialog (`filedialog.askopenfilename`) allowing users to browse and select any `.csv` dataset from their computer.
* Dropdown Combobox (`ttk.Combobox`) automatically populated with unique student names extracted from the file.
* Formatted Data Table (`ttk.Treeview`) with vertical scrollbars for clean visual grade report rendering.

How to Run

Running in Google Colab (CLI Version)
1. Open Google Colab and load `Lab9_File_Handling.ipynb`.
2. Execute the CLI code cell.
3. Click **Choose Files** when prompted to upload `course_lists.csv`.
4. Enter a student's name (or part of it) in the prompt to view their specific grade report.

**Running Locally (GUI Version)**
1. Ensure Python 3.x and `pandas` are installed:
   ```bash
   pip install pandas
