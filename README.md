# Active Directory & PowerShell Security Administration

I built this portfolio project from my existing TryHackMe learning notes and lab evidence. It documents how Active Directory administration, delegated support tasks, Group Policy, PowerShell fundamentals, and Windows domain authentication fit together.

## Project scope

This repository is based on two existing learning resources:

- [Active Directory & Windows Domain](https://app.notion.com/p/3b6f055fceba80b28ca4f08a5f542f54)
- [PowerShell](https://app.notion.com/p/3b9f055fceba8092be37e7a3c98ed0c3)

I organized the material into practical topics and linked the screenshots to the relevant procedures. I did not create additional lab results or claim production experience.

## What I documented

| Area | What I covered |
| --- | --- |
| Active Directory structure | Domains, domain controllers, AD objects, security principals, OUs, and security groups |
| OU protection | The purpose of protecting OUs against accidental deletion |
| Delegation of control | Delegating password-reset permissions to a Helpdesk account without granting Domain Admin rights |
| PowerShell administration | PowerShell objects, cmdlets, Verb-Noun syntax, command discovery, and the delegated password-reset workflow shown in my lab evidence |
| Group Policy | User and computer configuration, GPO scope, inheritance, SYSVOL, password policy, Control Panel restrictions, and automatic screen lock |
| Authentication | Kerberos ticket-based authentication and NetNTLM challenge-response authentication |

## Evidence

The `evidence/` directory is organized by topic. Each image is intended to show a specific action or concept from my existing lab work.

- [Active Directory evidence](evidence/01-active-directory/README.md)
- [PowerShell administration evidence](evidence/02-powershell/README.md)
- [Group Policy evidence](evidence/03-group-policy/README.md)
- [Authentication diagrams](evidence/04-authentication/README.md)

## Documentation

- [Active Directory administration](docs/active-directory.md)
- [PowerShell fundamentals and administration](docs/powershell.md)
- [Group Policy management](docs/group-policy.md)
- [Kerberos and NetNTLM](docs/authentication.md)

## Skills demonstrated

- Understanding of Active Directory domains, domain controllers, users, computers, groups, and OUs
- Understanding of least-privilege delegation for Helpdesk tasks
- Familiarity with PowerShell cmdlets and object-based pipelines
- Understanding of Group Policy configuration and refresh
- Understanding of Kerberos and NetNTLM authentication flows
- Organizing technical evidence and documenting administrative workflows

## Important scope note

This is a learning portfolio based on a TryHackMe training environment. It is not a production Active Directory deployment, a security audit, or evidence of managing a live enterprise domain.

## Sources

- TryHackMe learning notes: [6. Active Directory & Windows Domain](https://app.notion.com/p/3b6f055fceba80b28ca4f08a5f542f54)
- TryHackMe learning notes: [8. Powershell](https://app.notion.com/p/3b9f055fceba8092be37e7a3c98ed0c3)
