# HMSChainCode
 Smart Contract Documentation For HMS 

Introduction 

Smart Contract I.e chaincode for HMS is written in GoLang. All the patient’s confidential information to be stored and fetched in Blockchain as per smart contracts. 

Description 

1) Functionalities 

There are 3 main functionalities used  
a) Patient Data 

b) Session Details  

c) Document Info 
(ref line 23-45 in code for details) 

Which contains confidential data of patient and is stored in Blockchain 
 
Each patient will be having his own unique ID as KEY according to which data would be storing in Blockchain and every information related to that KEY (Patient) would be appended or updated w.r.t that key.  

 

2) Operations 

 

a) Create Patient() 

Patient when he gets registered his info is updated in network. 

There is also validation to check whether he is already registered or not 

b) Get History() 

It is fetching the entire history of patient from the blockchain network based on the Id which we will be giving as a input. 

c) update Profile() 

It is an additional features which is updated by doctor for his patient and it would also get updated in Blockchain w.r.t the key of the patient 

d) Tokensation() 

I have not yet added logic for tokenization as there is no proper set of documentation available in documentation I am researching on it but I have assigned a variable for it. It can also be created NodeJs end and could be stored in blockchain. 
 

As the above data is only the thing which is confidential and important and should be stored in a decentralized manner so that it could be easily made available to any once with proper security 
Rest of the part would be stored and handled in MongoDb. We can get clear idea once SDK and webservices are built. 

 

2) Queries for testing SmartContracts (Chaincode) 

===========createPatient==================   
peer chaincode invoke -n mycc -c '{"Args":["CreateUser","00", "risabh","15/11/1994"]}' -C myc
============readUser====================  
peer chaincode invoke -n mycc -c '{"Args":["readProduct", "00"]}' -C myc
==========GetHistoryForPatient===========  
peer chaincode invoke -n mycc -c '{"Args":["GetHistoryForPatient", "00"]}' -C myc
===========UpdateProfile================== 
peer chaincode invoke -n mycc -c '{"Args":  ["UpdateProfile","00","123","20/11/12","fever",`["paracetamol","dcold"]`,"500","ctscan"aasasasa","11/11/11"]}' -C myc
=========ValidateProfile==================  
peer chaincode invoke -n mycc -c '{"Args":["ValidateProfile","00"]}' -C myc
=============Range=========================
peer chaincode invoke -n mycc -c '{"Args":["getproductByRange","",""]}' -C myc 

 
