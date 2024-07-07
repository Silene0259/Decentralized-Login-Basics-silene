# Decentralized-Login-Basics-silene
This repository contains information related to creating a decentralized login system.

## Description

Ever wonder what it would be like if there were decentralized systems that run like any other system but allow logins/accounts to be done through a decentralized manner? This paper describes such a scenario and was first introduced in `September 2023` before OPRFs were a thing.

## Types of Decentralized Systems (silene-type)

* Decentralized Account Management (Login/Registration)
* Decentralized Mail (Messaging, Account Registration Messaging, Decentralized Email)
* Decentralized Certificate System
* Decentralized Search Engines
* Decentralized Domain Spaces

## Account-Management (Basics)

This system requires a **Decentralized Block Lattice** to be run underneath everything. It is powerful and useful for creating completely independent, decentralized systems that rely on decentralized programs to run.

### Pre-reqs

There exists a Block Lattice or Blockchain capable of doing the following operations. There can also exist a Virtual Machine that smart contracts run on to control this.

1. Client Requests Login To Decentralized Server
2. Server Sends Their Verifiable-Random-Function (VRF) token using as a seed the current login state in the block lattice
