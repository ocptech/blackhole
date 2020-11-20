# blackhole
Blackholing a list of IPs sourced from S3 bucket

This is complete package for NSO. Copy entire directory under ..../packages directory. 


This is a simple package to demonstrate NSO ability to solve different and diverse problems presented from customer.

Using Boto3 library (AWS provided) for python, the service created with this package:
- download a .txt file with a list of IPs form an amazon S3 bucket
- create an IP route pointing to a null interface in an IOS device for each IP in the list.





![Topology](https://github.com/cbottcher/blackhole/blob/main/Topology.png)



This is a very simple implementation, so please be aware of below considerations/pre-requisites. 

Please refer prerequisites.pdf for the initial setup for using the script:

- The S3 bucket provided in the example is not for public access, you need to provide your own one.
- Credentials for login to access the S3 bucket are implemented using "aws configure" application for Linux.
- IOS device and its NED must be working also in advance

NOTE: Cisco NSO should be installed and working. For Trial installation instructions and licences:
https://developer.cisco.com/docs/nso/#!getting-nso/getting-nso
or you can use NSO sandbox: 
https://devnetsandbox.cisco.com/RM/Diagram/Index/43964e62-a13c-4929-bde7-a2f68ad6b27c?diagramType=Topology 

[![published](https://static.production.devnetcloud.com/codeexchange/assets/images/devnet-published.svg)](https://developer.cisco.com/codeexchange/github/repo/cbottcher/blackhole)