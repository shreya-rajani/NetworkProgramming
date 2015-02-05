A DNS Client Using TCP and TCP/UDP Performance Comparison

The goal of this assignment is to design, execute, and document a set of experiments comparing the performance of TCP and UDP.  You will extend Lab 2 to use TCP for communication, then you will compare TCP and UDP using several metrics.  You will also analyze your network traffic using Wireshark.

Requirements

Extend Lab 2 so that it also takes as input, at the command line, a flag indicating whether TCP or UDP should be used for communication.  Your program will be run as follows:
java -cp lab3.jar DNSClient [tcp|udp] 8.8.8.8 www.cnn.com A
python DNSClient.py [tcp|udp] 8.8.8.8 www.cnn.com (Links to an external site.) A
Carefully read section 4.2 of RFC 1035 and make the appropriate modifications to enable TCP-based communication with a DNS server.
Execute the following experiments:
Response time - compare the response time for DNS queries sent via UDP versus TCP.
Make sure to do several tests and consider reporting min, max, and average.
Test against at least two different DNS servers.  Use traceroute to help you to reason about differences in response time between the two servers.
Loss rate - compare the loss rate seen in UDP to the retransmission rate observed in TCP.
Use the ID field for matching UDP responses with requests. 
You will need to send several messages in order to see loss.  Experiment to design your experiment.
Use the tcp.analysis filters in Wireshark to examine the TCP retransmission rate. 
Generate a PDF document describing your results.  You will have at least two graphs, one for each experiment.  You may certainly generate more graphs.  For each graph, you will have at least two paragraphs of description.  The first paragraph will describe the setup of the experiment, for example the IP address of the DNS server used.  The second paragraph will describe the results. 
Note: you must submit a class DNSClient that can be run as described above, but you are welcome to design a separate test harness that runs the experiments described above.
Submission

By the deadline, all source code and documentation must be checked in to the git repository at //cs621/lab3.
Your class files must be packaged into a jar named lab3.jar.  This jar file must be at the top level of the lab3 directory (e.g. //cs621/lab3/lab3.jar).
Provide a README that clearly indicates how to compile and run your program.  Include a run script for running your program on the CS lab machines.
Submit a document, in PDF format, describing the results of your experiments.
Late projects will receive a score of 0.
Projects that are submitted incorrectly will receive a deduction of up to 20%.  This includes incorrectly named directories and missing source files.  Double check your submission!
Grading Scheme

20 - Compiles and runs as specified
10 - Write up of results submitted correctly
10 - Design of code
10 - Correct functionality for both TCP and UDP requests
10 - Response time graph (sufficient data collected, graphed in an understandable way)
15 - Response time write up (clear description of the experiment including all assumptions and parameters, thorough analysis of results)
10 - Loss rate graph (sufficient data collected, graphed in an understandable way)
15 - Loss rate write up (clear description of the experiment including all assumptions and parameters, thorough analysis of results)
