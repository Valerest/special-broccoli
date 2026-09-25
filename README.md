Program Requirements
The main program requires a current version of Python.
It uses Python’s built-in csv library, so no additional libraries need to be installed to run the main program.
The main program accepts:
DAR files converted to CSV format; and
D2L grade reports converted to text format.
Example CSV and text files are included with the submission.
Two smaller supporting programs are also included to convert the original PDF grade reports into the file formats required by the main program:
the DAR converter changes a DAR PDF into a CSV file; and
the D2L converter changes a D2L PDF into a text file.
These supporting programs are separate from the main program and only need to be used when the original reports are in PDF format.
The converter programs require the following external libraries:
pypdf
pdfplumber
These libraries can be installed using:
pip install pypdf pdfplumber
File Setup
The main Python program and all DAR CSV or D2L text files should be stored in the same folder.
No individual file type is required. The program can run using:
only DAR files;
only D2L files; or
a combination of DAR and D2L files.
The program can also handle no files being entered, but will not run a grade analysis on them. 
How to Run the Main Program
Place the main Python file and the converted grade-report files in the same folder.
Open the main Python file in PyCharm or another Python editor.
Run the program.
Enter the complete filename of a DAR or D2L file, including its file extension. For example:
courses.csv

Continue entering filenames until all desired files have been entered.
Type done when finished entering files.
For each D2L course, enter the number of course credits when prompted.
Review the displayed course information.
Enter a desired overall average between 0% and 100%, inclusive.
Review the projected overall average and the average required on the remaining coursework.
Program Output
For each course, the program displays:
course name;
current grade;
number of credits; and
percentage of the course completed.
The program also displays:
the projected overall average;
the desired overall average; and
the average needed on the remaining coursework.
If the student has already earned enough marks to reach the desired average, the program displays a message explaining this.
If the desired average would require more than 100% on the remaining coursework, the program explains that the goal is currently out of reach and suggests retesting lower marks if retesting is permitted.
If all coursework is already complete, the program explains that there is no remaining coursework available to change the overall average.

Questions Answered by the Program
What is the student’s current grade in each course?
The program displays the current grade extracted from each DAR or D2L file.
For example the computer science file displays:
Current grade: 95.49 %

How much of each course has been completed?
DAR courses are considered 100% complete because only completed courses with final grades appear in the converted DAR file.
For D2L courses, the completion percentage is calculated using the total weight of the completed assessments found in the report.
For example the computer science course file displays:
Course completed: 65.0 %

What is the student’s projected overall average?
The program calculates a credit-weighted average using the student’s current grade and the number of credits assigned to each course.
This represents the projected overall average if the student continues earning approximately the same grades.
For example if I enter my DAR file the course will display: 
Projected overall average: 94.75 %
What average is needed on the remaining coursework?
The program uses the student’s desired overall average, completed coursework, remaining coursework, course grades, and course credits to calculate the average needed on all remaining assessments.
For example for the computer science file:
Average needed on remaining coursework: 96.95 %
