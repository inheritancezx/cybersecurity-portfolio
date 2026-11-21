# SIMPENAN Web: Cryptography Platform

[Back to portfolio](../../) | [Team repository](https://github.com/rajariandhana/simpenan) | [My fork](https://github.com/inheritancezx/simpenan)

## Objective
Build a full-stack web platform that demonstrates end-to-end secure data handling using RSA, AES and digital signature verification. This was the long-term team project for the Information Security course (EF234502) at Sepuluh Nopember Institute of Tech.

## My role
I led the development of the core project concept and framework, and oversaw the security flow across the web features. I also contributed to the core security implementation, including hybrid RSA/AES key sharing, server-side file authorization, and PDF signing. I also developed key validation workflows in Livewire, added ID-card handling to registration, and implemented account, file-type, dashboard, and download interface improvements.
The main repository belongs to my teammate `rajariandhana` which i forked to my public repository; the real repository remained private until now and is connected to the github classroom of the related course.

## Environment and tools
- Framework: Laravel 11 (PHP), Livewire, Tailwind CSS
- Cryptography: RSA, AES, and digital signatures

## Method
1. Designed the core concept and the security flow across all web features.
2. Implemented AES for encrypting data and RSA for key handling.
3. Implemented digital signature creation and verification.
4. Improved the design iteratively using feedback from teaching assistants and tutors.

## Results
- A working platform with secure handling applied across its features.
- Program output and report will be presented at the evidence folder

## What I would do differently

- used a different framework, probably using flask or node.js
- Generate a unique data key for every file and wrap that key with a user's public key. A single application-wide AES key or directly stored symmetric key would not isolate each user's files or support secure key rotation.
- Move cryptographic operations into dedicated services and define a consistent envelope format containing algorithm, nonce/IV, authentication tag, key identifier, and ciphertext version. Use Laravel configuration rather than direct `env()` calls inside controllers.
- Use signed, standards-based PDF signing or a maintained PDF-signature library, and verify the actual signed bytes and certificate chain. Keep signing certificates and private keys outside the web repository and storage directory.

## note
this assignment was previously made private per student code of conduct.
However, as the course had ended and that I have graduated, it is allowed to be publicized as a portfolio/own project.