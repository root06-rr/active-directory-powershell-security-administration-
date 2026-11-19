# PowerShell Fundamentals and Administration

## Overview

PowerShell is a command-line shell and scripting language used for administration and automation. Its cmdlets return structured objects rather than only plain text.

## Cmdlet naming

PowerShell cmdlets generally follow a Verb-Noun pattern.

Examples from my notes:

```powershell
Get-Content
Set-Location
Get-Date
Get-Process
Get-Service
```

The verb describes the action. The noun identifies the object or resource.

## Objects and the pipeline

A PowerShell object contains properties and methods. Cmdlets can pass objects through the pipeline so that later commands can filter, sort, or select information.

Examples covered in my notes:

```powershell
Get-ChildItem | Sort-Object Length -Descending
Get-ChildItem | Where-Object -Property Extension -eq ".txt"
Get-ChildItem | Select-Object Name, Length
```

## Command discovery and help

```powershell
Get-Command
Get-Help Get-Date
Get-Alias
```

These commands help identify available commands, read usage information, and inspect aliases.

## System and network information

My notes cover commands for viewing system information, local users, network configuration, processes, services, TCP connections, file hashes, and alternate data streams.

Examples include:

```powershell
Get-ComputerInfo
Get-LocalUser
Get-NetIPConfiguration
Get-NetIPAddress
Get-Process
Get-Service
Get-NetTCPConnection
Get-FileHash -Path <filepath>
Get-Item -Path <filepath> -Stream *
```

## Delegated Active Directory task

The Active Directory lab notes document a support workflow in which Phillip uses delegated permissions to perform a password reset through the Active Directory PowerShell module.

The evidence index records the session, password-reset action, and target login validation. The source notes do not include the literal `Set-ADAccountPassword` command text in their PowerShell fundamentals section. For that reason, this repository treats the screenshot as the evidence for the command used in the lab rather than presenting an unverified command line.

See [PowerShell evidence](../evidence/02-powershell/README.md).

## Source

[8. Powershell](https://app.notion.com/p/3b9f055fceba8092be37e7a3c98ed0c3)
