<h1>Task</h1>
<b>First step.</b>
Implement your SQLAlchemy models for the tables:

Student table;
Table of groups;
Table of teachers;
A table of subjects with an indication of the teacher who teaches the subject;
A table where each student has grades in subjects with an indication of when the grade was received;

<b>Second step</b>
Use alembic to create migrations in the database.

<b>Third step.</b>
Write the seed.py script and fill the resulting database with random data (~30-50 students, 3 groups, 5-8 subjects, 3-5 teachers, up to 20 grades for each student in all subjects). Use the Faker package for filling. When filling, use the SQLAlchemy session mechanism.

<b>The fourth step</b>
Make the following samples from the resulting database:

Find 5 students with the highest GPA in all subjects.
Find the student with the highest average score in a particular subject.
Find the average score in groups for a particular subject.
Find the average grade point average in a stream (across the entire grade table).
Find what courses a certain teacher teaches.
Find a list of students in a particular group.
Find the grades of students in a particular group in a particular subject.
Find the average grade given by a certain teacher in his/her subjects.
Find a list of courses that a particular student is taking.
Find the list of courses taught by a certain teacher to a certain student.

For queries, create a separate file my_select.py, which will contain 10 functions from select_1 to select_10. The functions should return the same result as the previous homework. When making queries, use the SQLAlchemy session mechanism.

<h2>Additional task</h2>

<b>The first part</b>
For the extra assignment, make the following queries of increased complexity:

The average grade that a certain teacher gives to a certain student.
The grades of students in a certain group in a certain subject at the last class.


<b>Second part.</b>
Instead of the seed.py script, think about and implement a full-fledged CLI program for CRUD operations with the database. Use the argparse module for this purpose.

Use the --action command or the shortened version -a for CRUD operations. And the --model (-m) command to specify which model the operation is to be performed on.


<h2>INFO</h2>

Examples of commands in the terminal.

Create a teacher
python main.py -a create -m Teacher -n 'Elton Pol'

Delete a teacher
python main.py -a remove -m Teacher --id 6

Show the list of teachers
python main.py -a list -m Teacher

Update teacher data
python main.py -a update -m Teacher --id 5 -n 'Mr. Roman Bortonovych'
