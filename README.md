# CryptoVison

MD5 Data Encryptor.

_The CryptoVision project was originally developed as part of a Computer Science BSc Degree._

## About

A segment of a larger piece of security suite software (CryptoVision) to allow data (images/text) to be encrypted/decrypted using an MD5 crypto algorithm (XOR).
CrytoVision is unique in the fact encrypted data can still be viewed after encryption.

![Encryption of the Bird test image](https://i.imgur.com/O07VD7z.png)

## Getting Started

The encryptor itself is a single Jar file however some test images/text are included. To run the encryptor, navigate to the folder in which the Jar is contained, and run the follow from a terminal/command line.

```java -jar CryptoVision.jar
```

You can specify the data file to process straight from the command line.

```java -jar CryptoVision.jar <path/to/file>
```

You can also specify a custom encryption key from the command line (recommended).

```java -jar CryptoVision.jar <path/to/file> <key>
```

## Process

- Data is loaded into the program
- Encryption key is converted into an MD5 hash to secure the key
- MD5 hash is converted into a seed (value used for consistent 'random' generation)
- Data is XOR'd with 'random' data
- Encrypted data is saved back to a file
- Decryption is possible due to 'random' data being replicated via the seed

## Repo

- `/src/`	
	CryptoVision source
- `/test/`	
	Sample test data
- `README.md`	
	This readme file
- `CryptoVision.jar`	
	The runnable data encryptor