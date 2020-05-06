# Web Security

* HTTPS - HyperText Transfer Protocol Secured
* SSL - Secure Sockets Layer
* IETF - Internet Engineering Task Force
* TLS - Transport Layer Security

* When you browse to a website without using https, you are opening up yourself to being eavesdropped on, which could include your password.

* Without the security of https, unencrypted messages can be intercepted and altered before reaching their final destination.

* Https uses SSL certificates to ensure you are connected with the exact reciever you want to be. This is a form of authentication.

* There are two types of algorithms for encryption
    * *Symmetric Key* algorithm - This method uses only one key to encrypt and decrypt the message. This message is sent with the ecnrypted message, and is also encrypted, which essentially means it is turned into unreadable scrambled letters and numbers.
        * These keys are hard to share and require you to be very careful.
    
    * *Asymmetric Keys* - Asymmetric keys utilize 2 different keys, one public and one private.
        * The public key can be shared with anyone and everyone, but messages that are 'locked' (encrpyted) with the public key, can only be opened with the private key.

* Your browser and the reciepient of the message have to make an agreement on how to communicate succesfully.
    * To do this, your browser sends a list of SSL and TLS versions and encryption algorithms, and the recipient chooses the best ones for the use case.
    * The recipient then chooses the best suited algorithms and creates a public key to be sent back to our browser.
    * If this public key matches what your browser expects, a *pre-master key* is created.
    * This pre-master key is then encrypted using your browsers public key and shared with the recipient, as a 'shared secret'.

* Certificate Authorities - 3rd party authority with 3 main objectives
    * Issuing Certificates
    * Confiriming Identity
    * Providing proof that the certificate is valid
