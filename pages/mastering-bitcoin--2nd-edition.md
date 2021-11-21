# Mastering Bitcoin, 2nd Edition

[> Home](../README.md)
## 4. Keys, Addresses



More precisely, the private key can be any number between 0 and n - 1 inclusive, where n is a constant (n = 1.1578 * 1077, slightly less than 2256) defined as the order of the elliptic curve used in bitcoin (see “Elliptic Curve Cryptography Explained”). ([link](https://learning.oreilly.com/library/view/-/9781491954379/ch04.html#27df0a38-842a-4631-862c-1361d5167bb6))


Vikram: [How does this prevent two people from having the same number?]


The private key must also be backed up and protected from accidental loss, because if it’s lost it cannot be recovered and the funds secured by it are forever lost, too. ([link](https://learning.oreilly.com/library/view/-/9781491954379/ch04.html#470ff5fa-e110-41c4-99ec-8ecd19d349a1))


The public key is used to receive funds, and the private key is used to sign transactions to spend the funds ([link](https://learning.oreilly.com/library/view/-/9781491954379/ch04.html#a56bcfe5-07ee-4f8e-ba80-0b4a3f07f265))


Bitcoin uses elliptic curve multiplication as the basis for its cryptography ([link](https://learning.oreilly.com/library/view/-/9781491954379/ch04.html#07c53675-82d1-469c-8246-126a1dfda459))


Ownership of bitcoin is established through digital keys, bitcoin addresses, and digital signatures. ([link](https://learning.oreilly.com/library/view/-/9781491954379/ch04.html#ec341917-1e24-4639-abaa-4dfdd9f40e71))

## 1. Introduction



The key innovation was to use a distributed computation system (called a “Proof-of-Work” algorithm) to conduct a global “election” every 10 minutes, allowing the decentralized network to arrive at consensus about the state of transactions ([link](https://learning.oreilly.com/library/view/-/9781491954379/ch01.html#99270f5a-af8f-45c2-87fb-c4064d5c7809))

[> Home](../README.md)