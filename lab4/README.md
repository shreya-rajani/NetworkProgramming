Again, thanks to Prof. Sami Rollins.

Lab 4 - Distributed Web Cache

The goals of this assignment are integrate the DNS tools you have developed into an application and give you experience using multicast for communication.  For this assignment, you will extend your Proxy Cache from Lab 1 to be a distributed, cooperative cache similar to Squid (Links to an external site.).  
Requirements

Service Discovery - You will use multicast-based DNS Service Discovery to discover other caches on the same LAN.  When your web proxy starts, it will query for other services of the same type and maintain a local cache of other nodes providing the web cache service.  Your proxy will also advertise its own service.  You will use the service type (Links to an external site.) cs621-cache.
You will follow the Exponential Back-off and Service Announcement algorithm implemented by Apple's Bonjour.  The algorithm is described here: http://developer.apple.com/library/mac/#documentation/Cocoa/Conceptual/NetServices/Articles/about.html (Links to an external site.)
You will follow the Suppression of Duplicate Responses algorithm implemented by Apple's Bonjour, also.  This algorithm is also described here: http://developer.apple.com/library/mac/#documentation/Cocoa/Conceptual/NetServices/Articles/about.html (Links to an external site.)
Page Retrieval - If a request experiences in a cache miss, your cache will first query other caches before making a request to the source.  If content is found at a peer cache, it will be retrieved from that cache, cached locally, and returned to the browser.  The remaining design and implementation choices are up to you.  You may, for example, use either unicast or multicast to query other caches, but remember that multicast is unreliable and should not be used to fetch the actual content.
[Extra-credit (up to 15 points)] Micro-benchmarks - You will explore the performance of your program by timing the following relevant operations.  The results of these experiments will be documented and submitted as a PDF.  Thoroughly explain the setup of your experiments and the results you report.  Use graphs and/or tables where appropriate.
time to fetch/return an object from the source.
time to return an object cached locally.
time to fetch/return an object from a sibling cache.
Demo Checklist

Launch proxy 1 (p1) and demonstrate that it advertises itself with a valid DNS packet using the Bonjour Service Announcement algorithm.  This should be demonstrable using Wireshark.
Launch p2 on a second machine and demonstrate that it discovers p1 and that p1 discovers p2.  It is recommended you demonstrate this via appropriate command line or logged output, but you can also implement some kind of administrative interface for your proxy.
Launch p3 on a third machine and demonstrate that all proxies discover all other proxies.  
Demonstrate that ongoing queries implement Suppression of Duplicate Responses.  This should be demonstrable using Wireshark.
Demonstrate a request for an object that must be retrieved from the source.  It is recommended you demonstrate this using appropriate command line or logged output at all proxies (e.g., all proxies log a cache miss for the object.
Demonstrate a request for an object that results in a hit at the proxy the browser/client is configured to use.   It is recommended you demonstrate this using appropriate command line or logged output at the proxy from which the request is made.
Demonstrate a request for an object that results in a miss at the proxy the browser/client is configured to use, but a hit at a sibling proxy.  It is recommended you demonstrate this using appropriate command line or logged output at both the proxy that experiences the miss and the proxy that experiences the hit.
Describe the algorithm you use to query sibling proxies.
Overview the design of your code.
Submission

By the deadline, all source code and documentation must be checked in to git repository at //cs621/lab4.
A demonstration to the TA is required.  Failure to demonstrate your work will result in a deduction of up to 20%. Scheduling will be available on Canvas on April 7.
If you are using Java, your class files must be packaged into a jar named lab4.jar.  This jar file must be at the top level of the lab4 directory.
Provide a README that clearly indicates how to compile and run your program. 
For the extra-credit, submit a document, in PDF format, describing the results of your experiments.
Late projects will receive a score of 0.
Projects that are submitted incorrectly will receive a deduction of up to 20%.  This includes incorrectly named directories and missing source files.  Double check your submission!
