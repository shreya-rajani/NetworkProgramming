Lab 1 - Proxy Server

Due - Monday February 10, 2014 - 11:59PM

The goal of this assignment is refresh your memory of socket programming and HTTP.  For this assignment, you will complete Socket Programming Assignment 4: Multi-threaded Web Proxy in Chapter 2 in the textbook. If you use Python, read Socket4_ProxyServer.pdfPreview the documentView in a new window. If you use Java, read here (Links to an external site.). 

Description

For full credit, you must implement caching as described in the Caching section and #3 of the Optional Exercises.
You may use a programming language other than Python or Java, but you must use raw sockets.  If you use a HTTP library you will not receive full credit for the assignment.
If you use Java, your program must run as described on the assignment page: java ProxyCache port
If you use Python or Java, you do not need to use the sample code provided on the website if you feel another design would be more appropriate.

You must include a README that clearly describes how to compile and run your program on the CS lab machines and a run script that will run your program on the lab machines.
Submission

By the deadline, all source code must be checked in to Git repository at /username/cs621/lab1.
Late projects will receive a score of 0.
Projects that are submitted incorrectly will receive a deduction of up to 20%.  This includes incorrectly named directories and missing source files.  Double check your submission!
Grading

20 points - Compiles and runs as specified (includes was submitted in the correct directory)
15 points - Correctly fetches uncached pages
15 points - Correctly returns cached pages
15 points - Saves objects to disk
15 points - Use of sockets (correct and well-designed solution)
10 points - Design of data structure
10 points - Code design
