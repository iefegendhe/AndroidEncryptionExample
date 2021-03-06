Android Encryption Example
========================

This is an encryption example of RSA and AES (CBC, ECB, CTR) 256 bit key on android with unit tests. I have 
tried to provide a good and secure example by showcasing:

* AES 256 bit key
* CBC/CTR/ECB example
* using salt for key derivation
* streams for arbitrary data sizes
* unit tests
* RSA 2048 bit
* Spongy Castle (Android version of Bouncy Castle encryption library)

The example encrypts the inputted string using AES, encrypts the key via RSA, and does the reverse when
the decrypt button is clicked.

Prerequisite
========================

In order to build the apk and run tests you must have the JCE (Java Cryptogrpahy Extension) Unlimited Strength policy jars installed for your JRE runtime.  

* JCE download for java 8: http://www.oracle.com/technetwork/java/javase/downloads/jce8-download-2133166.html

If you do not do this then you will see the error:
```
java.lang.RuntimeException: java.security.InvalidKeyException: Illegal key size or default parameters
```

Testing/Building
========================

To run the unit tests
```
./gradlew clean test
```

To build and install apk:
```
./gradlew clean installDebug
```

