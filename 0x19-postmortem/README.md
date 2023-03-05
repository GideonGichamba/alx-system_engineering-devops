 # Devschool Failure Report
<image src='./image.png' width="100%">

Last week it was reported that the devschool  platform was  returning error 5000 on all routes. It affected 80% of the platform user . The root cause was failure of our master server web-01

## Timeline
The error was realized on Friday 3rd March 2023 13:28 (East African Time) when our site reliability engineer Mr. sheezy  received a complain from one of the users and he  found out that the  master server was lagging in speed. He immediately  reported the issue to our engineers  and they decided to disconnect  the web-01 server for further analysis  and channeled all the request to a client server web-02. And they finished solving the problem on Friday 3rd March 2023 22:49 (East African Time)

## Root cause and resolution
Our devschool platform is served by two Ubuntu cloud server. The web-01 server was connected to serve all requests and it stopped functioning due to memory outage as a result of many requests  because during the previous test the client server web-02 was disconnected for temporary testing and was not connected to the load balancer afterwards .

The issue was  solved when the master sever was disconnected temporary foe memory clean up  and was connected back to the load balancer and round robin algorithm was  configured so that the mater and the client server receive equal amount of requests

## Measures against such problem in future
    • Always choose the best load balancing algorithm for your programs
    • always keep an eye on your program to ensure they are running  properly
    • have extra back-up  server to prevent your program from completely going offline during  an issue

###Devschool Platform Failure Report
image

Last week, there was an issue with the Devschool platform where all routes were returning error 5000, which affected 80% of the platform users. The root cause was identified as the failure of our master server, web-01.

Timeline
The error was discovered on Friday, April 29th, 2022 at 13:28 East African Time, when one of our users reported the issue to our site reliability engineer, Mr. Sheezy. Upon investigation, it was found that the master server was lagging in speed. Our engineers immediately disconnected the web-01 server for further analysis and redirected all requests to a client server, web-02. The problem was eventually resolved on the same day at 22:49 East African Time.

Root Cause and Resolution
Our Devschool platform is served by two Ubuntu cloud servers, with web-01 server connected to serve all requests. The server stopped functioning due to a memory outage, caused by an overload of requests. This was due to the client server, web-02, being temporarily disconnected during a previous test and not being reconnected to the load balancer. To resolve the issue, the master server was temporarily disconnected for memory cleanup and was then reconnected to the load balancer. A round-robin algorithm was configured to ensure that both the master and client servers received an equal amount of requests.

Measures to Prevent Future Issues
To prevent such issues from occurring in the future, we will take the following measures:

Choose the best load balancing algorithm for our programs
Monitor our programs regularly to ensure they are running properly
Have extra backup servers in place to prevent our programs from going completely offline during an issue.
