# HTTPS

[Source](https://howhttps.works/certificate-authorities/)
https://dnsimple.com/comics

## Why we need HTTPs

* Privacy: should that no one can eavesdrope your message.
* Integrity - Man in the middle attack. somebody else intercepted the message snd modified it.
* Identification- I can check if the message is coming from the right person. A digital signature attached to the message can identify the sender. This is possible with SSL Certificates.

## How HTTPS works

- How HTTPs provide all those 3 features - through encryption.
- There are two types of encryption algos - symmetric key algo and asymmetric key algo.

### Symmetric Key Algo

* only one key to encrypt and decrypt the message. the person who has the copy of the key can only decrypt the message. key + algo to encrypt the message.
  Issues:
    ** Hard to share. have to be super careful while distributing the key.

### Asymmetric Key Algo

* there we have 2 keys. one key is public and another key is private. they work together.
* You can share the public key with anyone.
* pug sends the public key to bird. Bird send the message back encrypting the message with public key. pug can read the message with his private key. Pug will use bird public key to send the message. This is good for privacy plus identification.

### Handshake

* browser communicates with the server and establish a secure communication.
* the negotiation between the server and the browser is called handshake. 

#### Steps

* Left Clap aka Client send SSL/TLS version along with encryption algo. wait for the answer from the computer.
* Right Clap aka Server choose the best one out of the sent ones based on his preference. and reply with the certificate with public key.
* Vertical shake aka Client key exchange: check server certificate to verify if they are legit. generate a pre-master to use it later. encrypt pre-master key with server public key and send it to the server. 
* shaka horitzontal rotation aka Change Cipher Spec: I use my private key to decrypt the pre-master key. 
* They both generate shared secret key. all the message will now be encrypted with shared secret now.

### protocols

* HTTP - is used to transfer the information between the web server and the browser. when the exchange of the data is encrypted with SSL/TLS then it is called HTTPS.  s stands for secure.
SSL is secure socket layer created by netscape. TLS = SSL 3.1 SSL was renamed to TLS by IETF. Latest TLS version is 1.3

### Certificate Authority

* 3rd party organization with 3 main objectives. 
1. Issuing certificates.
2. confirming the identity of the certificate owner. 
3. Providing proof that the certificate is valid.
