---
title: User authentication scheme using logins and passwords
summary: Consider the types of password authentication systems for users and identify their differences
tags:
  - Deep Learning
date: '2022-05-28'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: Photo by rawpixel on Unsplash
  focal_point: Smart

links:
  - icon: github
    icon_pack: fab
    name: Follow
    url: https://github.com/aaandrievskaya
url_code: ''
url_pdf: ''
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: example
---

## Introduction

The problem of the reliability of personal identification in modern conditions worries many authors, since the number of participants in electronic interaction in the modern world is steadily growing. Authentication is the basis for building a trusting relationship between the parties when they interact through open communication channels, in connection with which the role of authentication of participants becomes significant.

Authentication is the process of determining whether someone (or something) is who he or she is pretending to be. In the context of IT processes, this means that the credentials provided by the person requesting access to the resource are compared with the data held by the resource. If the information matches, the user is granted access. As a rule, authentication processes are associated with the following tasks: to provide authorized access, to establish trust relationships during remote access, to establish (identify) the identity of the owner of an electronic signature, etc.

## 1. Password authentication prototypes

### 1.1 Voice passwords

Speech passwords have found their application due to the absence of any additional means in establishing the belonging of a certain person to a specific group of people.
For example, in the medieval Spanish army there were cases when, at nightfall, nervous soldiers accidentally killed one of their own, mistaking them for an enemy. The military leaders soon devised a remedy for this problem: every day they chose a word that, in the form of a secret signal, would serve so that the soldiers of the same group could recognize each other.

This system played an indispensable role during the Civil War and the Great Patriotic War, as evidenced by numerous historical documents. The password and recall were set, among other things, for conducting telegraph negotiations along the line of military communications.

Passwords and reviews are often used in undercover intelligence. They are predetermined phrases by which you can recognize a scout or agent. Here, the verbal password is proof that the scout (agent) was confronted by exactly the person with whom the other could meet and work.

The password and the answer to it can be real. In this case, those who meet may have with them objects predetermined and known only to them, for example, combs, coins, banknotes, which may be the same or, on the contrary, different. In this case, the real password can be independent or supplement the verbal password.


### 1.2 Castles

A lock is a mechanical, electrical or electronic device that limits the possibility of unauthorized use of something.

The idea of ​​locks and keys to them arose with the advent of private property, when people began to think about how to protect it from outside encroachment.

The presence of a shared key made the locks less secure, as it reduced the degree of security. Special combination locks, opened by typing letters or numbers on rotating disks, appeared in Europe in the 17th century. The use of the lock code was the prototype for the introduction of the modern password, and the selection of the code was difficult. So, of interest is the Eureka combination lock, patented in the USA in 1862, in which, due to the large number of different letters and numbers, the number of possible combinations on the lock was 1,073,741,824.

Drawing an analogy between a lock code and a computer password, the former has advantages and disadvantages similar to a modern password. The advantages include the absence of a key that can be lost and which an attacker can copy in the absence of the owner; the ability to quickly change the code. The disadvantages are as follows: the code can be forgotten, but writing it down increases the likelihood that an outsider will recognize the code; the code can be peeped when entering; often dates of birth, addresses, well-known numbers are used as codes, which simplifies the selection of the code.

A variation of the combination lock is an electronic lock. An electronic lock is a high-tech device controlled by microprocessors and used to lock doors. In the presence of an electronic lock, a decision on the access of persons to the premises is made on the basis of signals from various sensors: magnetic card readers, barcodes, contact memory sensors, biometric sensors, dial pads, combinatorial fluorescent molecular sensors, remote control, etc.
In the future, electronic locks could compete with molecular locks, which have a sensor that responds not to a set of electrical signals from a keyboard or a reader, but to a set of chemicals.

## 2. Password authentication

The advent of computers led to the need to protect the information stored in them, as well as the creation of access control mechanisms to it, the main component of which was user authentication, one of which is password.
Fernando Corbato, a professor at the Massachusetts Institute of Technology, is considered the inventor of computer passwords. The use of passwords was required, in modern terms, to differentiate access of several users to the files of one computer. Putting a password on each individual user as a lock seemed like a very simple solution. Since there was no earlier documented use of a security system when using a computer, it is Corbato who is credited with being the first to put such a system on a computer. With the advent of personal computers in the 1980s. the password has become an integral part of business life, and over time, everyday life. It should be noted that the same time is considered the earliest when password theft was documented. These early passwords were simple and easy to save, as complex hacker networks and password cracking programs did not yet exist.
Password authentication is currently the most common method of protecting information. Authentication can take place using one-time and reusable passwords. A reusable password is set by the user, and the system stores it in the database. It is the same for every session. These include PIN codes, words, numbers, pattern keys. One-time passwords - different for each session. It can be an SMS with a code.

### 2.1 Reusable password authentication

One of the ways to authenticate in a computer system is to enter your user ID, colloquially called "login" (English login - username, account), and a password - some confidential information. A reliable (reference) login-password pair is stored in a special database (Fig. 1.).
Simple authentication has the following general algorithm:
1. The subject requests access to the system and enters a personal ID and password.
2. The unique data entered is sent to the authentication server, where it is compared with the reference data.
3. If the data matches the reference, authentication is considered successful, if there is a difference, the subject moves to the 1st step
The password entered by the subject can be transmitted over the network in two ways:
• Unencrypted, in the clear, based on the Password Authentication Protocol (PAP)
• Using SSL or TLS encryption. In this case, the unique data entered by the subject is transmitted securely over the network.

### 2.2 One Time Password Authentication

Having once obtained the subject's reusable password, the attacker has permanent access to the compromised confidential information. This problem is solved by using one-time passwords (OTP - One Time Password). The essence of this method is that the password is valid for only one login, with each subsequent access request, a new password is required. The authentication mechanism for one-time passwords can be implemented both in hardware (Fig. 2.) and in software.
Technologies for using one-time passwords can be divided into:
• Use of a pseudo-random number generator, common for the subject and the system
• Use of timestamps in conjunction with a universal time system
• Use of a database of random passwords, common for the subject and for the system
The first method uses a pseudo-random number generator with the same value for the subject and for the system. A subject-generated password can be passed to the system on consecutive use of a one-way function or on each new request based on unique information from a previous request.
The second method uses timestamps. An example of such technology is SecurID. It is based on the use of hardware keys and time synchronization. Authentication is based on the generation of random numbers at certain time intervals. The unique secret key is stored only in the system base and in the subject's hardware device. When the subject requests access to the system, he is prompted to enter, in addition to the PIN from his account, a randomly generated number displayed at that moment on the hardware device. The system matches the entered PIN and the subject's secret key from its database and generates a random number based on the parameters of the secret key from the database and the current time. Next, the identity of the generated number and the number entered by the subject is checked. It also checks the time when the number was generated on the server and on the user's hardware device.
The third method is based on a single database of passwords for the subject and the system and high-precision synchronization between them. In this case, each password from the set can be used only once. Due to this, even if an attacker intercepts the password used by the subject, it will no longer be valid.
Compared to using reusable passwords, one-time passwords provide a higher degree of security.

## 3. System security

The use of reusable passwords has a number of significant disadvantages. Firstly, the master password itself or its hashed image is stored on the authentication server. Often, the password is stored without cryptographic transformations, in system files. Having gained access to them, an attacker can easily get to confidential information. Secondly, the subject is forced to remember (or write down) his reusable password. An attacker can get it by simply applying the skills of social engineering, without any technical means. Thirdly, the security of the system is greatly reduced in the case when the subject chooses his own password. Often it turns out to be some word or combination of words present in the dictionary. In GOST 28147-89, the key length is 256 bits (32 bytes). When using a pseudo-random number generator, the key has good statistical properties. The password, which is, for example, a word from a dictionary, can be reduced to a pseudo-random number 16 bits long, which is 16 times shorter than the GOST key. Given enough time, an attacker can crack the password with a simple brute-force attack. The solution to this problem is the use of random passwords or a time limit on the validity of the subject's password, after which the password must be changed.

### 3.1 One-way functions

From the point of view of the best security when storing and transmitting passwords, one-way functions should be used. Typically, cryptographically strong hash functions are used for these purposes. In this case, the server stores only the image of the user's password that he entered earlier. Having received the password and having done its hash transformation, the system compares the result with the reference image stored in it. If they are identical, the passwords are the same. For an attacker who has gained access to the image, it is almost impossible to calculate the password itself, since there is no way to “decode” the password. Finding its original appearance in the image is possible only by enumeration.

### 3.2 Multi-factor authentication

Multi-Factor Authentication is a method in which a user needs to prove by two different factors that they are the owner of the account or that they are logging in in order to access an account or confirm a transaction with funds.
Among the types of multi-factor authentication, the most common two-factor authentication (2FA - 2-factor authentication) is a method in which the user must provide two different types of authentication data to gain access, for example, something known only to the user (password) and something inherent only user (fingerprint).
Access to resources through entering a login and password is one-factor authentication, since only one type of authentication data is used to enter - a password known to the user.

### 3.3 One-factor two-factor authentication

Due to the fact that smartphones have become an integral part of our lives, they have become one of the ways to confirm the identity of the user. They are tokens for accessing various resources. In this case, a one-time password is generated either using a special application, or comes via SMS - this is the easiest method for the user
Authentication goes like this:
1. The user enters the login and password specified during registration. If this pair is correct, the system sends a one-time password with a limited validity period.
2. The user enters a one-time password and, if it matches what the system sent, the user gets access to his account, funds or confirms the money transfer.
Even if an attacker obtains a username and password for an account (using malware, stealing a notebook with passwords, or using social engineering and phishing methods), after entering these data, the system will send a one-time code with a limited duration to the user's linked mobile phone. Without a one-time code, a fraudster will not be able to steal money.

## Conclusion

Tracing the history of the appearance of locks and keys to them, and then with the advent of computers - passwords, one can observe how people have always been interested in the safety of things first, and with the advent of the information age and information. This interest has led to the fact that the means that allow restricting access to the object of preservation are constantly changing and becoming more complicated. And every time, inventors, researchers, scientists were looking for how to improve the means of identification and authentication, which is happening to this day.

