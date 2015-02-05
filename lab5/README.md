The goal of this lab is for you to understand how the characteristics of the data and the characteristics of networks can change what is the optimal way of reliable data transfer. You will design your own reliable data transfer protocol over UDP. You will implement both server and client.

Your Server program will take as input at the command line the following items:

1. The port number to use

 

Your client program will take as input at the command line the following items:

1. The IP address of the server

2. The port number of the server

3. The name of the requested file

I will run your Server as follows

python server.py 8888

or java -cp lab5.jar Server 8888

I will run your client as follows

python client.py 192.168.1.12 8888 test.txt

or java -cp lab5.jar Client 192.168.1.12 8888 test.txt

The output of your Client program must include

1. Connection to the server was successful

2. File transfer has started or File not found

3. File transfer is complete

4. (Extra credit) how the file transfer progress between 2 and 3

Requirements

You must use UDP for communication.
You must use raw sockets for communication.
You may not use any libraries for reliable data transfer.  You are required to design the protocol on your own.
Submission

By the deadline, all source code must be checked in to Git at //cs621/lab5.
Submit README that explains how your protocol is designed, how your protocol reliably transfers data, and what libraries you used, if any.
If you are using Java, your class files must be packaged into a jar named lab5.jar.  This jar file must be at the top level of the lab2 directory (i.e., user/cs621/lab5/lab5.jar).
If you are not using Java or Python, include instructions in README that clearly indicates how to compile and run your program and include a run script for running your program on the CS lab machines.
Late projects will receive a score of 0.
Projects that are submitted incorrectly will receive a deduction of up to 20%.  This includes incorrectly named directories and missing source files and README.  Double check your submission!
Grading

1. (20 points) correct submission, README explains well.

2. (20 points) A text file

3. (20 points) A gzip file

4. (20 points) A movie file

5. (20 points) A large iso file

[Extra credit] 5 points for showing the file transfer progress correctly. Explain how you do this in README

[Extra credit] Your programs will compete over many different network conditions. If your program is the fastest in a category, you will win extra 5 points.
