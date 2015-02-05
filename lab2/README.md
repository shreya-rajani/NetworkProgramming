Thanks to: Prof. Rollins

The goals of this assignment are (1) to give you experience using UDP and (2) to familiarize you with implementing communication protocols, specifically DNS.  For this assignment, you will implement a basic DNS client that will use UDP to communicate with a DNS server.

Your program will take as input at the command line the following items:

the IP address of the DNS server
the domain name to look up
the type of query (e.g., [A, NS, MX])
I will run your program as follows (the command line items may take different values, including erroneous ones):

            python DNSClient.py 8.8.8.8 www.cnn.com A

or   java -cp lab2.jar DNSClient 8.8.8.8 www.cnn.com A



The output of your program will look similar to the output produced by dig (Links to an external site.).  You will print all of the data received in the query response. Here is a packat capture from dig, and when your program runs you can expect a similar request should be sent to 8.8.8.8. dig.pcapngView in a new window.

 

 

Requirements

You must use UDP for communication.
You must use raw sockets for communication.
You may not use any libraries for generating or parsing DNS packets.  You are required to generate the packets, in the correct format, on your own.
Suggestions

You will need to familiarize yourself with Section 4 of RFC 1035 (Links to an external site.) (http://www.ietf.org/rfc/rfc1035.txt).
You may want to consult http://www.zytrax.com/books/dns/ch15/ (Links to an external site.), particularly regarding the QNAME format.
Consider testing your program using the CS DNS server or Google's Public DNS (Links to an external site.) servers (http://code.google.com/speed/public-dns/).  
Do not use port 5353.
You are encouraged to create a modular library for generating/parsing DNS packets as you will use this code again in a later assignment.
You may use any programming language for this assignment, but remember that you will not receive full credit if you use existing DNS libraries.
Submission

By the deadline, all source code must be checked in to Git at //cs621/lab2.
Submit README that explains how your program is designed and what libraries you used, if any.
If you are using Java, your class files must be packaged into a jar named lab2.jar.  This jar file must be at the top level of the lab2 directory (i.e., user/cs621/lab2/lab2.jar).
If you are not using Java or Python, include instructions in README that clearly indicates how to compile and run your program and include a run script for running your program on the CS lab machines.
Late projects will receive a score of 0.
Projects that are submitted incorrectly will receive a deduction of up to 20%.  This includes incorrectly named directories and missing source files and README.  Double check your submission!
