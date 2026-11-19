# Group Policy Management

## Overview

Group Policy Objects (GPOs) allow administrators to centrally configure user and computer settings in an Active Directory environment.

A GPO has two main sections:

- **Computer Configuration:** Settings evaluated for computer objects.
- **User Configuration:** Settings evaluated for user accounts.

## GPO scope and processing

GPOs are linked to sites, domains, or OUs. Their settings apply according to the target object, the link location, security filtering, inheritance, and policy processing rules.

A computer configuration setting linked to an OU containing only user accounts is not applied to a computer object in that OU because there is no computer object there to process it.

Loopback processing is relevant when user settings need to be determined by the computer location rather than only the user's OU.

## SYSVOL

Domain controllers use the SYSVOL share to distribute Group Policy files and related domain content. The notes identify the default path as:

```text
C:\Windows\SYSVOL\sysvol\
```

## GPO management console

The Group Policy Management Console includes several useful tabs:

- **Scope:** Shows where a GPO is linked and its security filtering.
- **Details:** Shows GPO metadata and status.
- **Settings:** Displays a report of configured policy values.
- **Delegation:** Manages who can edit, view, or modify a GPO.

## Configuration examples in my lab notes

The existing evidence covers these GPO tasks:

1. Password policy change.
2. Restricting access to Control Panel.
3. Configuring automatic screen lock.

The related screenshots are listed in [03-group-policy](../evidence/03-group-policy/README.md).

## Refreshing Group Policy

The source notes include this command for forcing an immediate Group Policy refresh:

```powershell
gpupdate /force
```

The notes also describe user-targeted and computer-targeted refresh options. The primary command shown in the existing evidence is `gpupdate /force`.

## Source

[6. Active Directory & Windows Domain](https://app.notion.com/p/3b6f055fceba80b28ca4f08a5f542f54)
