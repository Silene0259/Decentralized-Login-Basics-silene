# Decentralized-Systems-Basics (silene-type) (`slinky` | `Sumatra`)

**Brand Name (of projects currently being developed):** `slinky`, `sumatra`, `yugen`, `nightshade`, `shativira`

This repository contains information related to creating a decentralized login system. It was created by `silene0259` and is part of a group of ongoing projects. This information is free-to-use and for research/academic purposes. This is currently being developed under the names `Slinky` and `Sumatra` and I am actively looking for open-source contributors.

## Description

Ever wonder what it would be like if there were decentralized systems that run like any other system but allow logins/accounts to be done through a decentralized manner? This paper describes such a scenario and was first introduced in `September 2023` before OPRFs were a thing. These will be implemented and will be able to be played around with on my website.

The main power behind this idea is Block Lattices which are powerful tools like blockchains but with different use-cases.

## Types of Decentralized Systems (silene-type)

* Decentralized Account Management without passwords (Login/Registration) (0x0000)
* Decentralized Domain Spaces using `Pivot System` (0x0001)

* Decentralized Mail (Messaging, Account Registration Messaging, Decentralized Email)
* Decentralized Certificate System
* Decentralized Search Engines
* Decentralized Captcha (using VDFs)
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

## Decentralized Domains using Pivot System (0x0001)

> Brand: `SlinkyDomains` | `SumatraDomains`

Domains or usernames are especially important when it comes to translating addresses. While most applications use the same type of system, unique usernames, discord, for example, goes through another approach by adding numbers to the end of usernames. A better system can be developed.

This is called the `Pivot System`, a two-layer way of dealing with this problem. In this solution, the following happens for a Pivot.

### Pivot System (PivSys)

> **Basic Format:** `<pivot-pub-key>@<id>`

> **Example:** `CE26A3907B44::id:63555`

A `pivot` is generated with some initial information. This information is crucial and is the basis of everything contained within that pivot. A VRF should also be used within the Pivot System. The pivot is a public-key that is used to determine the `current pivot` one is at.

A block lattice is used for send/receive blocks to confirm something is valid on the pivot-system. It basically assigns a `pivot address` as a signer and all other addresses as requesters who request to be on that pivot, needing to be digitally-signed on the block lattice. Due to the fact a block lattice is in order, a single number (id) can be used to represent the address.

#### Centralized-Pivot System

In the centralized-pivot system, there only one pivot point that can be contacted.

#### Third-Party Pivot System

In the third-party pivot system, there exists multiple pivots, all which can have different information/rules and sign different addresses. In this system, it is easily extendable and can allow different rules. It is open and can be implemented by many different people in different ways.

## Outline

There exists a `Pivot Point` that is the main pivot. A block lattice is constructed that verifies the digital signatures and order of the different domain spaces. A domain space is requested on the pivot by request. It is then kept as an integer on the block lattice.

1. A Pivot Point (PP) is generated by a user. This pivot point is the main focus of all and contains within it all the information that is needed.
2. A Block Lattice is constructed using that pivot point public-key.
3. A send is sent to the address that the user wants the domain space on. The Pivot Point Address (PPA) can choose whether they want to accept it or deny it while still maintaining the order of the chain even if it is out of order.
4. When the send block is received and signed by the pivot point address, it is then validated as a legitimate domain. It can be accessed through integer or through its domain space.

## Decentralized Bot Detection

A simple, decentralized captcha can be created by having a current login state chain

---

## Technology Used

### Distributed Hash Tables

DHTs are used all throughout the process.

### Verifiable-Random-Functions (VRF)

Verifiable-Random-Functions
