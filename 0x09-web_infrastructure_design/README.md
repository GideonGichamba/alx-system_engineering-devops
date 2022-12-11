# Web infrastructure design

## What’s an A record?
A record maps domain name to IPV4 of the computer hosting the domain name.
An A record uses a domain name to find the IP address of a computer connected to the internet

## Canonical Name record(CNAME record)
is a type of resource record in the Domain Name System (DNS) that maps one domain name (an alias) to another (the canonical name)

NAME                    TYPE   VALUE
--------------------------------------------------
bar.example.com.       CNAME  foo.example.com.
foo.example.com.       A      192.0.2.23

when an A record lookup for bar.example.com is carried out, the resolver will see a CNAME record and restart the checking at foo.example.com and will then return 192.0.2.23. 

## MX record
A mail exchanger record (MX record) specifies the mail server responsible for accepting email messages on behalf of a domain name. It is a resource record in the Domain Name System (DNS).

## TXT record
is a type of resource record in the Domain name system (DNS) used to provide the ability to associate arbitrary text with a host or other name, such as human readable information about a server, network, data center, or other accounting information

## What Is Round Robin DNS?
Round robin DNS is nothing but a simple technique of load balancing various Internet services such as Web server, e-mail server by creating multiple DNS A records with the same name.

## What’s an NS Record?
An NS record delegates a subdomain to a set of name servers

## What’s an SOA record?
An SOA record is a Start of Authority. Every domain must have a Start of Authority record at the cutover point where the domain is delegated from its parent domain.
The root domain and sub domain - differences

## What is a Database
A database is information that is set up for easy access, management and updating.

## What’s the difference between a web server and an app server?
```web server``` process HTTP request by responding with HTML pages
```APP serer``` serves business logic to the program through varius protocals


## Monitoring
Just as the heart monitor in a hospital that is making sure that a patient’s heart is beating and at the right beat, software monitoring will watch computer metrics, record them, and emit an alert if something is unusual or that could make the computer not work properly happens.
1. Newrelic
2. Datadog
3. Uptime Robot
4. Wave front
5. Nagios

## What are containers and why do you need them?
Containers are a solution to the problem of how to get software to run reliably when moved from one computing environment to another. Here's what you need to know about this popular technology. 
### Virtual machine


## single point of failure (SPOF) 
is a part of a system that, if it fails, will stop the entire system from working.
