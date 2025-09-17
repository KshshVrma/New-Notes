is a way of authentication where :
there are 2 components:

user ->uses private key
server-> uses public key

when the user wants to connect to the server in that case the server generated a string (cryptic) and later encrypts the string using public key,,. and now sends this encrypted string to the user, who uses his private key to decrypt the encrypted string and hence sends some calculated value back to the server which determines if the sent string is correct or not. 

for different os  , there are different way's to calculate this ssh string , eg in mac: terminal
linux: terminal, windows putty.


[[A gentle introduction to SAML  SSOReady]]