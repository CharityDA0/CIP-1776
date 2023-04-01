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
Growing dissatisfaction with the governance model proposed in CIP1694 has splintered the Cardano community with divisive argumentation and rampant proliferation of misinformation on both sides of the debate. The model proposed by IO, while a commendable attempt to provide a first step to create a technically functional model of governance, fails to bring within its scope a mechanism for the drafting of the Cardano constitution despite its reliance on a constitutional committee. Further, while calling for the Cardano community to “think deeply about the processes for handling the creation of governance actions that are specified in (CIP 1694) In particular, the role of Project Catalyst in creating treasury withdrawal actions” it fails to bring the observed outcome resulting from four years of treasury experimentation into the scope of foundational governance. Finally, the membership of the constitutional committee is dismissed as “an off-chain issue”, despite such a committee being  pivotal to the proper functioning of the governance model.

## Goal
The goal of this CIP is to lay down a functional foundation for decentralized decision-making. This CIP describes a model for on-chain governance that is both technically and legislatively complete and (unlike other proposed models of governance) without any missing dependencies for a functional mechanism of minimum viable governance. This model leverages the existing Cardano governance mechanism scheme, correctly utilizing the seven existing governance keys. It aims to provide a tangible, scalable foundation that is technically achievable within a reasonable timeframe for any competent world leading blockchain development organization.

# Current governance mechanism design
The seven-key on-chain Cardano governance system, established during the Shelley ledger phase, possesses the ability to:

    1. Alter protocol parameter values, including the initiation of "hard forks."
    2. Move ADA between reserves and the treasury, as well as the withdrawal of ADA from these sources.

Under the existing framework, initiating governance actions necessitates special transactions with Quorum-Many authorizations from the governance keys (5 of the 7 on the Cardano mainnet). The transaction body contains fields detailing the proposed governance action, such as amending protocol parameters or initiating fund transfers. Each transaction can prompt only one type of governance action, but an individual action can produce multiple effects (e.g., modifying two or more protocol parameters).

Transaction body field no. 6 is utilized for protocol parameter updates. Meanwhile, Move Instantaneous Rewards (MIR) certificates are employed for handling treasury and reserve movements. Authorized governance actions are executed at epoch boundaries (when they are enacted).

## Hard Forks
Changing the major protocol version enables Cardano to enact controlled hard forks. This type of protocol parameter update therefore has a special status, since stake pools must upgrade their node versions to support the new protocol version once the hard fork is enacted.

## Limitations of the Shelley Governance Model
As we progress towards the Voltaire era, this proposal aims to remedy several limitations of the current design through the application of a minimum viable governance approach. Offering a simple, scalable, mutable model for governance is impossible under the Shelly model and thus an alternative is required.  

The Shelley governance model does not provide an avenue for active on-chain engagement from Ada holders. Although protocol changes often result from discussions with selected community members, the process is primarily driven by the founding entities as IOG, the Cardano Foundation, and Emurgo hold between them all seven governance keys.

Treasury movements are a crucial and delicate matter, but they can be difficult to monitor. It is essential to establish greater transparency and additional layers of control over these transactions.

Hard forks, which require special handling by SPOs, are not distinguished from other protocol parameter alterations.

Lastly, while Cardano's founding entities and many community members generally share a somewhat unified vision for the project, many other stakeholders in the system do not. Utilizing the Cardano blockchain to permanently record the shared Cardano ethos as a formal Cardano Constitution makes sense. 

# Out of scope

The following topics are considered to be out of the scope of this proposal.

## Legal Issues
This CIP does not acknowledge the jurisdiction of any nation state or legal authority for the enforcement of any action in relation to the Cardano blockchain due its nature as a censorship resistant distributed network.

# Terminology

This CIP introduces the concept of 'Voltaire completeness'. This expression is used to mean "Satisfies all requirements for a viable governance model with no outstanding dependencies". For example, a proposal that called for a constitutional committee to oversee a constitution, but provides neither a constitution nor the ability within the proposed governance model to formally implement one, would not be considered to be 'Voltaire-complete'. This can be likened to the term 'Turing Complete' in computer science.

# Specification

●       The Cardano Constitution

●       Proposal & Ratification of Legislation

-----       The Standard Model

-----        The Treasury Model

●       Governance Bodies

-----       The Constitutional Court

-----       Stake Pool Operators

-----      Delegated Representatives
	
●       Technical Implementation

●      Frequently Asked Questions

●      Licence & Copyright

# The Cardano Constitution

For the purposes of this CIP we introduce a minimum viable constitution and a mechanism by which amendments may be added:

	Decentralization: may it serve as our North Star, our guiding light, and our highest virtue.

This foundation allows us to proceed with our minimum viable governance model and sets out a framework for the CIP 1776 governance model. The first amendment to this constitution shall be a substantive document of monumental significance, and it and all subsequent amendments will follow the standard model for ratification.

A minimum viable constitution must be outlined prior to the establishment of a governance system that has a body to govern over the constitutionality of any given governance action. It is proposed that this constitution be recorded on-chain. 

The wording of this minimum viable constitution has been explicitly crafted to be universally acceptable to the community while still providing the minimum required framework for the further ratification of governance actions on-chain. 

# Proposal & Ratification of Legislation
For a decentralized and balanced model of governance all governance actions must be easily understood by the relevant stakeholders in the network. By providing a clear and easy-to-understand model for governance ratification, we aim to ensure that all stakeholders in the Cardano network can participate in the governance process and have a say in the network's future development. This helps to ensure that the governance process is decentralized and balanced, with no single entity or group holding too much power or influence.

Achieving the delicate balance between accessibility and quality control is paramount for a well-functioning governance model. To that end, we propose a solution that leverages the expertise and vested interests of members in the Cardano community who are already financially incentivized to uphold the network's decentralization, the Stake Pool Operators. 


While any DRep may put forward a governance proposal, it requires a single eligible Stake Pool Operator to second that proposal for it to move to the next stage of governance. SPOs may put forward one proposal per epoch. 

This organically forms a soft-oversight on proposals, while also encouraging members who cannot get the support of Stake Pool Operators to start their own stake pool and leverage their ADA or the ADA of their supporters to become eligible to submit their own governance proposal.

To be ratified, a governance action must be approved by all three governance bodies using their votes. Once ratified, the action may be enacted on-chain.

Here we introduce the Standard Model for the ratification of governance actions:

## The Standard Model

The Standard Model of Ratification has five distinct stages and follows the same process regardless of the contents of the vote. The progression through each stage occurs at the epoch boundary. Multiple proposals at different stages may run in parallel. The Standard Model may not move funds from the Cardano treasury. 

**Epoch 1: Proposal Submission**
Any Cardano User may submit a proposal to any Cardano Stake Pool Operator. Of all the proposals the SPO receives in a 5-day window they may choose to submit one (or make no submission) to proceed to epoch 2 of governance. 

**Epoch 2: SPO Voting**
In the second round, eligible stake pool operators declare their vote. Stake Pool Operators that meet the eligibility requirements may cast a single vote. This vote must be cast on-chain during epoch 2 of governance. Success or failure shall be determined by a simple majority of all votes cast. 

**Epoch 3: DRep Voting Intent Declaration**
In the third round, DReps declare their voting intention. Upon declaration, voting intention can not be changed AND will be enacted as declared. The weighting of this voting intention is determined in Epoch 4

**Epoch 4: Vote Calculation**
In the fourth round the vote calculation takes place. If during the third round ADA users disagree with the voting declaration of their DRep, the ADA holder may redelegate their ADA. This avoids elected representatives voting against the intention of their supporters. Success or failure shall be determined by a simple majority of all votes cast.

**Epoch 5: Constitutional Court Ruling**
In the fifth and final round of the constitutional court votes to determine the constitutionality of proposals before them. The constitutional court may take up to 5 epochs to determine the constitutionality of a proposal before ratifying the action. Success or failure shall be determined by a 5-2 majority or greater.


This model is designed to allow the Cardano blockchain to respond dynamically to unforeseen future events that may bring the blockchain into jeopardy, be this quantum attacks, technical issues identified in legacy code, or attacks on the network. Additionally, all governance undergoes substantial balanced oversight and the issue of centralization of power and influence in the network is resolved.

##   The Treasury Model


The treasury model is detailed in CIP1215 and must not be implemented until after the ratification of a Constitutional amendment. The reasons for this are twofold; to ensure a constitutional framework for the ratification of treasury actions is in place prior to the execution of financial actions, and to allow for the community to properly scrutinize the treasury model for potential attack vectors prior to implementation. 

# The Constitutional Court

The Constitutional Court shall be composed of seven elected representatives and shall be collectively and individually responsible for ensuring the constitution of Cardano is respected. They shall be elected as the highest seven (7) DReps by stake amount under the cascading delegation governance model detailed in the Delegated Representatives section below.

One of the main concerns when creating a body such as The Constitutional Court is to prevent the centralization of power. Therefore, it has been proposed that The Constitutional Court will act only as a body with the powers to rule on the constitutionality of any proposal before them. This means that they will not have the power to directly approve or reject a proposal without the former ratification of both the lower and upper houses of governance, but rather will ensure that the proposal aligns with the Cardano Constitution prior to its formal ratification.  

The Constitutional Court will play a crucial role in maintaining the integrity of the Cardano governance system. They will review proposals approved by both the DReps and the SPOs and determine if they are in line with the values and principles outlined in the Cardano Constitution. This will ensure that the Cardano community is able to govern itself effectively and in a manner that is transparent and fair. 

Any DRep, be they an individual, committee, organization, non-profit group, or any other entity may occupy one of the ‘seats’ on the Constitutional Court provided they gather enough stake under the DRep model outlined below. Upon becoming a member of The Constitutional Court, their vote weighting as a DRep is instead converted into a single binary approve/disapprove vote of which five (5) of seven (7) members of The Constitutional Court must approve. 

This vital feature of the Constitutional Court prevents the centralization of power that could otherwise occur under other models, preventing a single group or small group of actors controlling both the voting share (DReps) and the oversight body (CC) at the same time. This counteracts the risk of DRep hyper centralization that forms under other governance proposals by redefining the influence that the top-seven DReps have over the network as a whole. Where we acknowledge that there will likely be DReps that are also SPO’s, this model carefully balances powers between general ADA holders, DReps, and the Constitutional Court resulting in substantially better prospects when aiming to create a decentralized governance model. 

While the principal number of seats on the Constitutional Court is seven (7), this may be altered by the ratification of a subsequent proposal. 

# Stake Pool Operators

Stake Pool Operators (SPOs) play a critical role in the Cardano governance system. SPOs are responsible for creating and maintaining the blocks that make up the Cardano blockchain. They are also responsible for participating in the governance process by voting on proposals during the second stage of the Standard Model and hold the unique position of gatekeeping low-quality / dangerous proposals from consideration by the other two houses of governance.

Mindful of the importance of not directly disenfranchising small Stake Pool Operators, while also ensuring fair representation for established Stake Pool Operators, to be eligible to vote or second a governance proposal in any given EPOCH an SPO much have minted at least one block in the epoch directly preceding their governance action. 

SPOs are selected by ADA holders who delegate their stake to a particular pool. The more stake a pool has, the more likely it is to be selected to create a block, and the more rewards it will receive. This incentivizes SPOs to provide reliable and secure infrastructure for the Cardano network. Stake Pool Operators are not obliged to participate in governance, however the existing incentive structure of Cardano directly aligns SPOs with the incentive for good governance. 

Under the cascading delegation governance model, SPOs may also delegate their pledge a DRep or vote with it directly, effectively giving them a say in the governance process beyond just their individual vote. However, SPOs are not able to leverage the delegation to their pool for voting beyond their single vote on matters in the Upper Chamber of governance, ie; for/against proposals and seconding one proposal per epoch. 

It is important to note that under the Standard Model, SPOs cannot move funds from the Cardano treasury. This ensures that the treasury remains secure and prevents any potential abuse of power by SPOs. However, once the treasury model is implemented, SPOs will have a direct role in the allocation of funds, making their role in the governance process even more critical. This role is balanced by the power of the DReps and Constitutional Court. 

# Delegated Representatives

Under this model, Delegated Representatives (DReps) act as the lower chamber of governance, casting votes based on the total ADA holdings they represent. Any Cardano user may choose to represent themselves as a DRep, and the process of delegating to a DRep is technically similar to delegating to a stake pool.

In addition to representing themselves, users may also delegate their voting rights to any other user wallet. The collective voting power of a group of users can also be delegated to another user through a cascading governance model. This allows for a more decentralized and democratic governance system, where all ADA holders have a say in the decision-making process. 

# Frequently Asked Questions

With due respect to the guidance from IO to give opposing arguments the strongest possible case in consideration, a process commonly known as ‘steel manning’, we ask that argumentation on this matter is done on the facts, not with rhetoric, name calling, or from a disingenuous premise. We all have the same goal of seeing this blockchain succeed. 

# Licence & Copyright
© EveryEpoch Limited (Company Number 14324429) - All Rights Reserved







