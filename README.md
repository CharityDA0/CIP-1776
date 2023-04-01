---
CIP: 1776
Title: CIP 1776: A Better Model For Decentralized Governance Version 0.5
Authors:
    - Thomas Stokes <info@eutxo.pro>
Contribtors:
    - Various Parties to be credited later
Implementors: N/A
Discussions:
    - TBD
Status: TBD
Created: 2023-01-22
License: All Rights Reserved
---

# CIP 1776: A Better Model For Decentralized Governance 

## Abstract
CIP 1776 proposes a comprehensive, decentralized, and balanced on-chain governance mechanism for the Cardano network. By balancing voting leverage between The Constitutional Court, Stake Pool Operators, and Delegated Representatives, this proposal seeks to create a system that ensures no single entity or group holds too much power or influence over the network's decision-making process. Furthermore, the proposal introduces a minimum viable Cardano Constitution, providing a guiding framework for governance actions and decisions.

We propose a modular system of governance and call for a revision of Cardano's on-chain governance system to support this proposal. Under our proposal, any Cardano user will be able to submit a governance action for consideration. The ratification of governance actions will be the responsibility of the following parties:

    1. Voters & Delegated Representatives (DReps)
    2. Stake Pool Operators (SPO)
    3. The Constitutional Court (CC)

Every governance action must be ratified by all three of these governance bodies using their votes. Ratified actions may then be enacted on-chain, following a set of well-defined rules.

The Stake Pool operators shall act as the upper chamber of governance each casting a single vote on governance matters while satisfying the eligibility requirements for participation. The existence of multi-pool operators has been accounted for in the extensive testing of this governance model and is balanced by the legislation ratification requirements for Delegation Representatives. 

Delegated Representatives shall act as the lower chamber of governance, each casting votes as weighted by their total ADA holdings, as a whole number of Lovelace. All cardano users may choose to represent themselves. Under this model, delegating to a DRep follows a technically similar model as delegating to a stake pool. Users may delegate their voting rights to any other user wallet. Additionally, users may delegate their collective voting power (their own ADA + all ADA delegated to them by others) to another user under a cascading governance model. Institutional holders, exchanges, and enterprise addresses, and individuals with substantial ADA holding have been accounted for in the extensive testing of this governance model and are balanced by both the legislation ratification requirements for the Stake Pool Operators and the electoral process for The Constitutional Court. 

The  Constitutional Court shall be composed of seven independently elected representatives responsible for adjudicating the constitutionality of all motions approved by Stake Pool Operators and Delegated Representatives and ratified or overridden accordingly. These may take the form of individuals, organizations, constitutional committees, or any combination of such groups able to meet and maintain the requirements for positioning as a keyholder on the Constitutional Court.

# Motivation: why is this CIP necessary?

## Motivation
Growing dissatisfaction with the governance model proposed in CIP1694 has splintered the Cardano community with divisive argumentation and rampant proliferation of misinformation on both sides of the debate. The model proposed by IO, while a commendable attempt to provide a first step to create a technically functional model of governance, fails to bring within its scope a mechanism for the drafting of the Cardano constitution despite its reliance on a constitutional committee. Further, while calling for the Cardano community to “think deeply about the processes for handling the creation of governance actions that are specified in (CIP 1694) In particular, the role of Project Catalyst in creating treasury withdrawal actions” it fails to bring the observed outcome resulting from four years of treasury experimentation into the scope of foundational governance. Finally, the membership of the constitutional committee is somewhat flippantly dismissed as “an off-chain issue”, despite such a committee being (under the CIP1694 model) pivotal to the proper functioning of the governance model, with the risk of a perpetual dissatisfaction in said appointed committee(s) grinding on chain governance to a halt.

## Goal
The goal of this CIP is to lay down a functional foundation for decentralized decision-making. This CIP describes a model for on-chain governance that is both technically and legislatively complete and (unlike other proposed models of governance) without any missing dependencies for a functional mechanism of minimum viable governance. This model leverages the existing Cardano governance mechanism scheme, correctly utilizing the seven existing governance keys. It aims to provide a tangible, scalable foundation that is technically achievable within a reasonable timeframe for any competent world leading blockchain development organization.

While this proposal is presented as a “logically feasible and complete’’ model, Version 0.5 is not presented as a ‘technically complete’ model. This is to allow for community consultation on the best technical approach to overcoming specific technical problems. The model presented here assumes that Input Output Global is  technically competent and that the Cardano blockchain ‘solves’ the blockchain trilemma of security, scalability, and decentralization.


