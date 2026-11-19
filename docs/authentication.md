# Kerberos and NetNTLM Authentication

## Overview

The Active Directory notes compare two Windows authentication approaches:

- **Kerberos:** Ticket-based authentication used as the default authentication protocol in contemporary Windows domain environments.
- **NetNTLM:** A challenge-response authentication protocol retained mainly for backward compatibility.

## Kerberos

Kerberos uses a Key Distribution Center (KDC) on the Domain Controller. The notes describe the following stages:

1. **AS-REQ and AS-REP:** The client requests authentication and receives a Ticket Granting Ticket (TGT).
2. **TGS-REQ and TGS-REP:** The client presents its TGT to request a service ticket for a specific service.
3. **AP-REQ:** The client presents the service ticket to the target service.

The TGT is protected using the `krbtgt` account key. A service ticket is associated with the service identified by its Service Principal Name (SPN).

## NetNTLM

NetNTLM uses a challenge-response exchange. The server provides a challenge and the client returns a response derived from its credential material. The raw password is not sent as part of the challenge-response exchange.

## High-level comparison

| Area | Kerberos | NetNTLM |
| --- | --- | --- |
| Authentication model | Ticket-based | Challenge-response |
| Main domain component | Key Distribution Center | Challenge-response exchange |
| Service access | Uses service tickets | Uses a response for the authentication exchange |
| Role in Windows environments | Primary domain authentication protocol | Retained for compatibility |

## Evidence

The original Active Directory notes include authentication diagrams for Kerberos and NetNTLM. They are indexed in [04-authentication](../evidence/04-authentication/README.md).

## Source

[6. Active Directory & Windows Domain](https://app.notion.com/p/3b6f055fceba80b28ca4f08a5f542f54)
