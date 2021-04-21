# Blackhole
Blackholing a list of IPs sourced from S3 bucket

## The requets:
Request from customer was to automatize a current manual process that mainly consist in:
- Download a .txt file from an AWS S3 bucket.
- Using the list of IPs in the file create a route in a cisco IOS device

![Request](https://github.com/cbottcher/blackhole/blob/main/Request.png)


## The solution:

Create a NSO service (python+template)

Using Boto3 library (AWS provided) for python, the service created with this package:
- download a .txt file with a list of IPs form an amazon S3 bucket
- create an IP route pointing to a null interface in an IOS device for each IP in the list.



![Topology](https://github.com/cbottcher/blackhole/blob/main/Topology.png)


NOTE:
- This is complete package for NSO. Copy entire directory under ..../packages directory. 
- This is a simple package (PoC grade) to demonstrate NSO ability to solve the request. Some extra work is needed for production
- Please refer to "prerequisites.pdf" for the initial setup for using the script.
- The S3 bucket provided in the example is not for public access, you need to provide your own one.
- Credentials for login to access the S3 bucket are implemented using "aws configure" application for Linux.
- IOS device and its NED must be working also in advance

NOTE: Cisco NSO should be installed and working. For Trial installation instructions and licences:
https://developer.cisco.com/docs/nso/#!getting-nso/getting-nso
or you can use NSO sandbox: 
https://devnetsandbox.cisco.com/RM/Diagram/Index/43964e62-a13c-4929-bde7-a2f68ad6b27c?diagramType=Topology 

[![published](https://static.production.devnetcloud.com/codeexchange/assets/images/devnet-published.svg)](https://developer.cisco.com/codeexchange/github/repo/ocptech/blackhole)
