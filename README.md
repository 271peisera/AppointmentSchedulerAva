# Appointment_Scheduler-Student
﻿SMART APPOINTMENT SCHEDULER - STUDENT STARTER
=============================================


CONTENTS (all in ONE folder when extracted)
  Appointment.java             - PROVIDED; do not edit
  AppointmentScheduler.java    - FIVE TODO methods to complete
  SchedulerMain.java           - PROVIDED console menu and startup/save I/O
  data/seed_schedule.txt       - starting schedule; do not edit
  BST_Appointment_Scheduler_Student_Directions.docx - assignment


SETUP
1. Extract this ZIP to a new folder.
2. In VS Code, File > Open Folder, and select THAT folder directly.
   The data folder must be in the same folder as the three .java files.
3. Run SchedulerMain.java (or in the terminal: javac *.java && java SchedulerMain).
4. Expected first message: Loaded 5 appointments from data/seed_schedule.txt


ONLY EDIT AppointmentScheduler.java.
The menu and initial file loading work before any TODO methods are completed.
Saving will not overwrite an earlier saved file until write() is implemented.
When working, save writes data/saved_schedule.txt; the next run loads that first.


ALL TIMES ARE 24-HOUR HH:MM. This is a single-day calendar, 08:00 to 17:00.

1. How does a TreeSet differ from an ArrayList in how it stores and organizes elements?
treeSet is a sorted collection that stores elements in a balanced binary search tree, automatically maintaining order and ensuring that there are no duplicate elements. 

2. What does the floor() method return? What does floor() return if there is no appointment starting at or before the requested time?
the floor() method returns the greatest element in the TreeSet that is less than or equal to the specified element. If there is no appointment starting at or before the requested time, floor() returns null.

3. What does the ceiling() method return? What does ceiling() return if there is no appointment starting at or after the requested time?
the ceiling() method returns the least element in the TreeSet that is greater than or equal to the specified element. If there is no appointment starting at or after the requested time, ceiling() returns null.

4. Why might these methods be useful in an appointment scheduling program?
these methods are useful in an appointment scheduling program because they allow the program to quickly find the appointments that are immediately before and after a requested time.

5. Suppose our calendar contains these appointments:
Start
End
9:00 AM
9:40 AM
10:15 AM
11:00 AM
11:30 AM
12:00 PM

  
If we attempt to schedule an appointment beginning at 10:00 AM, which existing appointments would floor() and ceiling() return, assuming appointments are ordered by start time?
if we attempt to schedule an appointment beginning at 10:00 AM, floor() would return the appointment starting at 9:40 AM                                                                                                                         and ceiling() would return the appointment starting at 10:15 AM.


1. Explain how floor() and ceiling() allow your scheduling program to detect overlapping appointments. Why is checking these two appointments sufficient, rather than checking every appointment in the calendar? 

floor() and ceiling() methods in a TreeSet allow the scheduling program to efficiently find the appointments that are immediately before and after a requested time. The floor() method returns the greatest appointment that is less than or equal to the requested time, while the ceiling() method returns the least appointment that is greater than or equal to the requested time. Checking these two appointments is sufficient because if the requested time overlaps with any existing appointment, it will either overlap with the appointment returned by floor() or the one returned by ceiling().

2. Why is a TreeSet (balanced binary search tree) more efficient than an unsorted ArrayList for finding the appointments immediately 

before and after a requested time? Compare their Big O time complexities and explain why this matters as the schedule grows. 
A TreeSet has a time complexity of O(log n) for operations like floor() and ceiling(), where n is the number of appointments in the set. This means that as the number of appointments grows, the time it takes to find the appointments immediately before and after a requested time increases logarithmically, which is relatively efficient.

3. Why is it unnecessary to save the exact shape of TreeSet’s internal tree?

It is unnecessary to save the exact shape of TreeSet’s internal tree because the structure of the tree is determined by the order of the elements and their natural ordering or comparator.
