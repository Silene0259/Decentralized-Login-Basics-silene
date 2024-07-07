# Decentralized-Systems-Basics (silene-type)
This repository contains information related to creating a decentralized login system. It was created by `silene0259` and is part of a group of ongoing projects. This information is free-to-use and for research/academic purposes. This is currently being developed under the names `Slinky` and `Sumatra` and I am actively looking for open-source contributors.

## Description

Ever wonder what it would be like if there were decentralized systems that run like any other system but allow logins/accounts to be done through a decentralized manner? This paper describes such a scenario and was first introduced in `September 2023` before OPRFs were a thing. These will be implemented and will be able to be played around with on my website.

The main power behind this idea is Block Lattices which are powerful tools like blockchains but with different use-cases.

## Types of Decentralized Systems (silene-type)

* Decentralized Account Management without passwords (Login/Registration) (0x0000)
* Decentralized Domain Spaces using Pivot System (0x0001)

* Decentralized Mail (Messaging, Account Registration Messaging, Decentralized Email)
* Decentralized Certificate System
* Decentralized Search Engines
* Decentralized Bot Detection (using VDFs)
* Decentralized Storage

## Decentralized Account Management without contacting server or requiring password (0x0000)

This system requires a **Decentralized Block Lattice** to be run underneath everything and makes use of verifiable-random-functions (VRFs) and **beacons**. It also uses extensive use of Public-Key Cryptography like Digital Signatures to run. It is powerful and useful for creating completely independent, decentralized systems that rely on decentralized programs to run.

### Outline

1. Client Requests Login To **Decentralized Server** (without ever contacting server)
2. Server Sends Their **Verifiable-Random-Function (VRF) token** using as a seed the `current login state` in the block lattice. This block lattice is known as the `Login State Lattice (LSL)` and contains the current seed that must be used to login. This is useful for keeping time and login states valid while rejecting older ones or newer ones while still providing decentralized randomness.
3. Client Signs The **VRF Token** using their `secret key` that is displayed (or the public key of that secret key to be exact) under their account
4. A `Beacon` verifies VRF Randomness with the current state and client signature.
5. After verification, a transaction is made legitimazing the login/registration to the account at the current time.
6. Beacon allows login to occur on chain and sends tx to client on chain using a send/receive block
7. Client confirms tx with receive block and is now registered/logged-in

In this system, the server and client never have to meet.

## Decentralized Domains using Pivot System (

> Brand: `SlinkyDomains` | `SumatraDomains`

Domains or usernames are especially important when it comes to translating addresses. While most applications use the same type of system, unique usernames, discord, for example, goes through another approach by adding numbers to the end of usernames. A better system can be developed.


---

## Technology Used

### Distributed Hash Tables

DHTs are used all throughout the process.

### Verifiable-Random-Functions (VRF)

Verifiable-Random-Functions
