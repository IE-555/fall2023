# Homework 5 -- NumPy

- Due Monday, December 4, by 12:00pm (noon)

--- 

Sometimes source data aren't in a format that we would've designed.  The purpose of this assignment is to help you practice using `numpy` and to work with poorly formatted data.


You need to write one (1) function that calculates some statistics about student grades in a particular course.

- Your function should be in a Python script named `UCASEUBUSERNAME_grades.py` (replace `UCASEUBUSERNAME` with your UB user name in all caps).
- Within this python script, you should write a function named `gradeInfo`
- The `gradeInfo()` function will be called as follows: 
    - `gradeInfo(filename, numExams, hwWeight)`
        - See `UCASEUBUSERNAME_grades.py` for information about these three input parameters.

Your `gradeInfo()` function should do the following:

1. `Import the given `.csv` file.  See `grades_example.csv`, which describes the structure of input files.

2. Return the following five (5) pieces of information, **in this order**:
    1. Find the average of HW1. 
        - Return this as a scalar value in the range `[0, 100]``.

    1. Sort the grades in descending order for HW2 (best grades first). 
        - Return as a `n x 2` numpy array.  There are `n` rows, where each row is a student.  The first column returned should be the student ID, the second column is the score on HW2 (as a score in the range `[0, 100]`).
	
    1. Find the students who made 90 or above on both HWs 1 and 3. 
        - Return as a 1-dimensional numpy array, just containing ID numbers.

    1. Find the number of students who made 80 or below on HW1 and 90 or above on HW2. 
        - Return as a scalar integer.
	
    1. Each homework is equally weighted.  Find each student's current average grade, rounded to 1 decimal place, in the range `[0, 100]`. 
        - Return as a `n x 2` numpy array.  There are `n` rows in the source data, where each row is a unique student.  The first column to be returned is the student ID, the second column is the weighted score in the range `[0, 100]`.
            - For example, suppose a student had the following scores: 
                - Homework:  9/10, 4/5, 35/50.  Exam1:	85/100 
		
            - If `hwWeight = 0.4`, the student's average grade is
				`( ( (9/10 + 4/5 + 35/50)/3 ) * 0.4 + ( (85/100)/1 ) * (1 - 0.4) ) * 100 = 83.0`
	



	



	
	