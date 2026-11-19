# Active Directory Administration

## Overview

Active Directory (AD) is a central directory service used to manage network identities and resources. A Windows domain groups users and computers under centralized administration. A Domain Controller runs Active Directory Domain Services and handles domain authentication and directory operations.

## Core objects

- **User accounts:** Represent people or service identities that need domain access.
- **Computer accounts:** Represent domain-joined computers. A computer account commonly uses the computer name followed by `$`.
- **Security groups:** Allow permissions to be assigned to multiple users or computers.
- **Organizational Units (OUs):** Organize directory objects and provide a location for Group Policy links and delegated administration.

A security principal is an identity that can be authenticated and assigned permissions. User accounts, computer accounts, and security groups can act as security principals.

## OUs and security groups

| Organizational Unit | Security group |
| --- | --- |
| Organizes directory objects | Groups identities for permission assignment |
| Can be used to link Group Policy | Can be granted access to resources |
| An object belongs to one OU at a time | An object can belong to multiple groups |

## Protecting OUs from accidental deletion

Active Directory can protect OUs against accidental deletion. This safety setting helps prevent an administrator from unintentionally removing an organizational unit.

My existing lab notes include an OU deletion-protection example. The matching screenshot belongs in [01-active-directory](../evidence/01-active-directory/README.md).

## Delegation of control

Delegation allows an administrator to assign a limited administrative task to another account. For example, a Helpdesk account can be granted permission to reset passwords for users in a selected OU without receiving full Domain Admin privileges.

My lab notes document the delegation workflow through Active Directory Users and Computers (ADUC). The evidence is linked from the [Active Directory evidence index](../evidence/01-active-directory/README.md).

## Delegated password reset using PowerShell

The lab workflow documents a support session using the account Phillip, followed by a password reset through the Active Directory PowerShell module and a target login validation step.

The evidence is separated into three stages:

1. Initial remote session as the support account.
2. Password reset through PowerShell.
3. Target login validation.

See the [PowerShell evidence index](../evidence/02-powershell/README.md).

The source notes describe the use of Active Directory PowerShell commands. The exact command parameters should be read from the original screenshot rather than reconstructed from memory.

## Source

[6. Active Directory & Windows Domain](https://app.notion.com/p/3b6f055fceba80b28ca4f08a5f542f54)
