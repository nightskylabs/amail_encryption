# amail encryption backend

This is the open-sourced code for the double encyption done by Night Sky Labs for the mails on the Amail dapp on Azero Network. 

Goal: To add a second layer of encryption at the web2 layer for the messages being stored  
Procedure: The message (currently a Max of 500 characters) is taken as input, and a 165 character key is generated using pseudorandom computations. This is broken into 3 smaller keys of equal length, and they are key-expanded and used in either:  
1. 3DES cipher
2. Rabbit cipher
3. AES cipher

Since which cipher is used for which packet is NOT stored on the database, a malicious hacker would need to hack not just the database, but also the Azero Network to be able to extract anything but heavily encoded packets of text from Amail. This makes it more secure than any purely web 2 or web 3 mailing application.
