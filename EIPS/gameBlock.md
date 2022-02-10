---
eip: <to be assigned>
title: Gameblock
description: Building block for class of trustless games
author: 0xrin
discussions-to: <URL>
status: Draft
type: Standards Track
category (*only required for Standards Track): ERC
created: 2022-02-10
requires (*optional): <EIP number(s)>
---

## Abstract
This EIP introduces a standard that serves as a building block for a class of trustless games. Hence the name.
It is an abstract contract that can be extended to construct games that:
- Would require simultaneous action (for example rock paper scissors)
- Where information is concealed
  - Provided the winner needs to reveal it to prove victory
  - Provided the opponent does not also need to reveal something they concealed

## Motivation
The motivation behind this proposal is to establish and encourage a standard for games to use that fit the above criteria.
This is beneficial to the community because it allows for more interoperability and trust.
Say a new game contract is released. If it can and is constructed out of a Gameblock, users will be more willig to trust the contract knowing that it follows a predefined standard.

## Specification
The key words “MUST”, “MUST NOT”, “REQUIRED”, “SHALL”, “SHALL NOT”, “SHOULD”, “SHOULD NOT”, “RECOMMENDED”, “MAY”, and “OPTIONAL” in this document are to be interpreted as described in RFC 2119.

The technical specification should describe the syntax and semantics of any new feature. The specification should be detailed enough to allow competing, interoperable implementations for any of the current Ethereum platforms (go-ethereum, parity, cpp-ethereum, ethereumj, ethereumjs, and [others](https://github.com/ethereum/wiki/wiki/Clients)).

## Rationale
The rationale fleshes out the specification by describing what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work, e.g. how the feature is supported in other languages.
The rationale behind the standard emerged from the realization, while constructing a simple game contract, that the underlying structure of the game can be abstracted tosuit a class of games.
The datatype used for the states array, bytes32, was chosen to support as many state types as possible. Initially a string was chosen, which could work. Bytes32 is more flexible though at the cost of more work for the implementer, which seems like a reasonable tradeoff.


## Backwards Compatibility
Since this is a new and relative unextensible standard, backwards compatibility can not be addressed at this time.

## Test Cases
This proposal does not introduce any consensus changes.

## Reference Implementation
Reference, example implementation can be found here https://github.com/0xrin1/Gameblock/blob/master/src/Gameblock.sol

## Security Considerations
Security considerations here depend fully on the implementer of the standard.
Gameblocks themselves are simple but their use depends entirely on their implementation.

## Copyright
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
