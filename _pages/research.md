---
title: "Research"
permalink: /research/
author_profile: true
---

# Research

## Research Vision

My research focuses on privacy-enhancing technologies that reconcile
privacy, security, and accountability.

Rather than treating privacy as the complete concealment of
information, I investigate how systems can protect legitimate users
while enabling narrowly scoped auditing, tracing, or revocation when
misuse is confirmed.

To date, my main research has addressed accountable anonymous digital
payments, selective tracing, secure processing of sensitive data, and
privacy-preserving authentication.

More recently, I have been extending these research questions to
Industrial Internet of Things, robotics, and Physical AI.

Across these domains, my research is guided by a common question:

> How can a system provide the information necessary for security and
> accountability without exposing more personal or identifying
> information than necessary?

---

## Accountable Anonymous Digital Payments

Digital payment systems must protect the privacy of legitimate users
while preventing their anonymity from being exploited for money
laundering, terrorist financing, double spending, and other illicit
activities.

My research investigates accountable anonymous electronic cash and
offline payment protocols that provide payer and payee anonymity and
transaction unlinkability during normal operation.

At the same time, when a specific coin is associated with confirmed
misuse, the system should support efficient and selective tracing
without exposing unrelated users or inspecting the entire transaction
history.

In my recent work, I designed an accountable anonymous offline
electronic cash system using BBS+ signatures, ElGamal encryption, and
zero-knowledge proofs.

The system supports:

- Payer and payee anonymity
- Transaction unlinkability
- Offline payments
- Detection of double spending
- Selective forward and backward coin tracing
- Identification of relevant transaction participants
- Protection of unrelated users during an investigation

The objective is not to provide an authority with unrestricted access
to every transaction. Instead, the tracing authority should be able to
investigate only the coin or transaction associated with a legitimate
and predefined tracing condition.

---

## Privacy-Preserving Auditing and Selective Tracing

Privacy and financial accountability are often treated as competing
requirements.

Fully traceable payment systems can expose the complete financial
history of ordinary users, while fully anonymous systems can make it
difficult to investigate illegal financial activity.

I study cryptographic mechanisms that balance these requirements
through selective auditing and cryptographically constrained tracing.

My research considers how these mechanisms may contribute to future
digital payment infrastructures, including electronic cash,
stablecoins, and central bank digital currencies.

The long-term goal is to enable:

1. Privacy for honest users during ordinary payments
2. Efficient investigation of specific illicit transactions
3. Protection against mass surveillance
4. Clear separation between normal verification and exceptional tracing
5. Compatibility with AML and CTF requirements

I am also interested in how technical mechanisms interact with
regulatory requirements for stablecoins, cross-chain transactions, and
AI-operated financial services.

---

## Privacy-Preserving Authentication and Revocation for IIoT

My current research also examines anonymous authentication in
Industrial Internet of Things environments.

Devices operating in factories, edge networks, and cross-domain
systems must demonstrate that they possess valid permissions.
However, repeatedly disclosing a permanent device identifier allows
their activities to be linked and tracked.

Anonymous credentials, group signatures, and zero-knowledge proofs can
protect device identity, but strong anonymity also creates a practical
revocation problem.

When a device is compromised, the system must be able to revoke its
authentication capability without revealing or testing the identities
of all honest devices.

I am currently investigating mechanisms that combine:

- Anonymous credentials
- Zero-knowledge proofs
- Group signatures
- Physically unclonable functions
- Merkle-tree-based authorization
- Dynamic or universal accumulators
- Anonymous revocation tokens
- Verifiable revocation states

The main objective is to allow an edge server or verifier to determine
whether an anonymously authenticating device remains valid, while
preventing the verifier from learning the device’s permanent identity.

I am particularly interested in efficient revocation mechanisms that
can disable the credentials or authentication structures associated
with a compromised device without requiring exhaustive searches over
all authentication logs.

---

## Selective Protection of Sensitive Data

My earlier research addressed how sensitive data can remain useful
while only privacy-related information is protected.

### Privacy-Preserving Surveillance Video

I studied selective encryption and decryption of privacy-sensitive
regions in surveillance videos.

The proposed system identifies facial regions, assigns an
entity-specific identifier and encryption key to each person, and
allows only the target entity to be selectively decrypted.

The system also applies post-processing to protect facial regions that
are missed by the recognition model.

This research demonstrated that privacy mechanisms must account for
the uncertainty and recognition failures of AI models rather than
assuming perfect perception.

### Efficient Updates to Encrypted Data

I also studied the protection of continuously updated data in cloud
collaboration environments.

The proposed encryption mechanism divides encrypted data into bundles
and updates only the modified portions instead of decrypting and
re-encrypting the entire dataset.

This work considers both security and practical efficiency for
dynamic encrypted data.

These studies provide a foundation for protecting data generated by
systems that continuously observe, update, and exchange information.

---

## Emerging Research Direction: Privacy for Physical AI

Building on my previous work in accountable anonymity, anonymous
authentication, selective encryption, and dynamic data protection, I
aim to extend privacy-enhancing technologies to Physical AI.

Robots and embodied AI systems perceive humans through cameras,
microphones, and various sensors. They may process faces, voices,
locations, movements, biometric information, and contextual
relationships.

These systems must use some of this information to operate safely.
However, they should not retain, share, or reveal all observed
information in an identifiable form.

My future research will focus on two main problems.

### Privacy-Preserving Robot Authentication

Robots and autonomous agents should be able to prove that they possess
valid permissions without repeatedly disclosing permanent identifiers.

I aim to investigate authentication systems that provide:

- Anonymous authorization
- Interaction unlinkability
- Efficient revocation
- Conditional accountability
- Resistance to device impersonation
- Protection of honest robots during investigations

This direction extends my current work on anonymous authentication and
revocation in IIoT environments.

### Privacy-Preserving Multimodal Perception

I also aim to study how robots can protect the visual, audio,
biometric, and contextual information they collect.

Possible research questions include:

- How can a robot process visual information without retaining
  identifiable facial data?
- How can sensitive voice segments be selectively encrypted?
- How should a system respond when an AI model fails to detect
  privacy-sensitive information?
- How can data related to one incident be disclosed without revealing
  unrelated observations?
- How can access to robot-collected data be limited by purpose, role,
  and time?

---

## Long-Term Goal

My research trajectory connects digital payments, IIoT authentication,
and Physical AI through a shared principle:

> Privacy should be preserved during normal operation, while
> accountability should be activated only under limited, legitimate,
> and technically enforceable conditions.

In digital payment systems, this means protecting ordinary users while
supporting selective investigation of illicit financial activity.

In IIoT environments, this means authenticating devices anonymously
while enabling efficient revocation of compromised devices.

In Physical AI, this means allowing robots to perceive and cooperate
without creating unrestricted surveillance of humans.

My long-term goal is to develop cryptographic and privacy-preserving
mechanisms that support trustworthy digital infrastructure and safe,
private, and accountable coexistence between humans and intelligent
machines.
