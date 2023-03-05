# Devschool Failure Report
<image src='./image.png' width="100%">

Last week it was reported that the devschool  platform was  returning error 5000 on all routes. It affected 80% of the platform user . The root cause was failure of our master server web-01

## Timeline
The error was realized on Friday 29th  April 2022 13:28 (East African Time) when our site reliability engineer Mr. sheezy  received a complain from one of the users and he  found out that the  master server was lagging in speed. He immediately  reported the issue to our engineers  and they decided to disconnect  the web-01 server for further analysis  and channeled all the request to a client server web-02. And they finished solving the problem on Friday 29th April 2022 22:49 (East African Time)

## Root cause and resolution
Our devschool platform is served by two Ubuntu cloud server. The web-01 server was connected to serve all requests and it stopped functioning due to memory outage as a result of many requests  because during the previous test the client server web-02 was disconnected for temporary testing and was not connected to the load balancer afterwards .

The issue was  solved when the master sever was disconnected temporary foe memory clean up  and was connected back to the load balancer and round robin algorithm was  configured so that the mater and the client server receive equal amount of requests 

## Measures against such problem in future
    • Always choose the best load balancing algorithm for your programs
    • always keep an eye on your program to ensure they are running  properly
    • have extra back-up  server to prevent your program from completely going offline during  an issue 