# CPSC/ECE3220 Project1 Testcases

This folder contains all the testing code for TaskA and TaskB. All the test code should run from the project1 root directory.

# 1. Installing python dependencies

The test cases uses python for testing the code. So, Python3 and pip is required for this.  To install all the required dependencies:
```
 pip install -r ./test/requirement.txt
```

# 2. Testing code

For part1A we always recompile the code and test using the files in folder testfiles.
To test part1A, run from project1 folder, the command:
```
pytest ./test/test_p1a_git.py
```
To test part1B, run from project1 folder, the command:
```
pytest ./test/test_p1b_git.py
```

For Part1A, we test the main functionality, Error cases and Edge cases as mentioned in the Part1A documentation.\
For Part1B, we have added  a simple `testgetprocs.c` file in the user functions. The file create various process and call getprocs method to get all the processes.\
Pytest command shows a passed test case with `.` a Failed one with `F`. If the test cases fails, pytest will show the test function as well as the output it received after running the test command.
