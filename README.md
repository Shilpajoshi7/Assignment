# Assignment
Online Technical Challenge

# _Challenge 1_ 
---
Here I am using ARM Template IAC concept to create a 3-tier architecture using Microsoft Azure cloud.

I am creating 3 VM's   
1) Front End Layer 2) Back End Layer 3) Database Layer

ARM Template will create multiple resources (i.e. V.M., NSG, NIC, Public IP, Availability Set, etc.) to set up whole infrastructure 
for a 3-tier application.

I have created multiple NSG in this template so that only required ports should be open. For Example, I don't need to RDP in front end layer, so I will block RDP port, and I need to open internet and https port for the same I will create the policy in ARM template to open port 443 for front end layer.







# _Challenge 2_ 
---
The function is to get the metadata from the aws portal for each individual ec2 instance. 

Using this I can fetch the metadata in two ways:
1) I can fetch whole metadata in json object format. 
To fetch the whole metadata we need to run
   
    ``python get_metadata.py -o all``


2) I can fetch single metadata just by entering the key. Let I want to get the "ami-id" data from the instance. To get this 
we need to run **(Bonus Point)**
   
    `python get_metadata.py -o key -k ami-id`





# _Challenge 3_ 
---
The function is to get value from the nested object. In this function I am passing pass the two arguments:
1) Object
2) Key

I have nested object in which I have given a key and for that key I have to find the value from that nested object.

To run this I need to run 

`python main.py -o "{'x':{'y':{'z':'a'}}}" -k "x/y/z"`

By running this command we will get output as shown below:

`2021-03-26 01:55:30 INFO     ===> data : {'x': {'y': {'z': 'a'}}} 
2021-03-26 01:55:30 INFO     ===> key_input_list : ['x', 'y', 'z']
2021-03-26 01:55:30 INFO     ===> output : a`


I have also created some unit test cases for the same that you can find in `unitTest.py` file.
It consists of multiple unit test cases scenario for challenge 3.  
