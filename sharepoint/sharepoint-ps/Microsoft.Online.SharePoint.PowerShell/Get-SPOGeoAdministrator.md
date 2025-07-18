---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spogeoadministrator
applicable: SharePoint Online
title: Get-SPOGeoAdministrator
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Get-SPOGeoAdministrator

## SYNOPSIS

This cmdlet returns the SharePoint Online user or security group accounts with Global Admin privileges in the current multi-geo tenant.

## SYNTAX

```
Get-SPOGeoAdministrator [<CommonParameters>]
```

## DESCRIPTION

You may only use parameters from one parameter set and you may not combine parameters from different parameter sets.
For more information about how to use parameter sets, see [Cmdlet parameter sets](/powershell/scripting/developer/cmdlet/cmdlet-parameter-sets).

The `Get-SPOGeoAdministrator` cmdlet has a single parameter set and matches a user or a list of users which has the ability to do changes globally in the geo location that you are connected to.

Running this cmdlet on a non-multi-geo tenant organization will return error -4.

You must be a SharePoint Online administrator and you must have a the Multi-Geo Capabilities in Office 365 service plan to run the `Get-SPOGeoAdministrator` cmdlet.

For permissions and the most current information about Windows PowerShell for SharePoint Online, see the online documentation at [https://go.microsoft.com/fwlink/p/?LinkId=251832](https://go.microsoft.com/fwlink/p/?LinkId=251832).

## EXAMPLES

### Example 1

```powershell
Get-SPOGeoAdministrator
```

This cmdlet will output a SharePoint Online user or security group that is Multi-Geo administrators on the current multi-geo tenant.

## PARAMETERS

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Add or remove a geo administrator](/Office365/Enterprise/add-a-sharepoint-geo-admin)

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Get-SPOAppErrors](Get-SPOAppErrors.md)

[Add-SPOGeoAdministrator](Add-SPOGeoAdministrator.md)

[Remove-SPOGeoAdministrator](Remove-SPOGeoAdministrator.md)
