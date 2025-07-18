---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spogeostoragequota
applicable: SharePoint Online
title: Get-SPOGeoStorageQuota
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Get-SPOGeoStorageQuota

## SYNOPSIS

This cmdlet gets the storage quota on a multi-geo tenant.

## SYNTAX

```
Get-SPOGeoStorageQuota [-AllLocations] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet shows the storage on the current location or all locations in a multi-geo tenant.

This cmdlet requires a connection to a multi-geo tenant to run correctly. You must be a SharePoint Online Administrator to get the storage on the current location or all locations in a multi-geo SPO tenant.

## EXAMPLES

### EXAMPLE 1

```Powershell
Get-SPOGeoStorageQuota -AllLocations
```

Get the storage size quota of all locations.

### EXAMPLE 2

```Powershell
Get-SPOGeoStorageQuota
```

Get the storage size quota of the current location.

## PARAMETERS

### -AllLocations

> Applicable: SharePoint Online

Use this parameter to retrieve the storage size quota of all locations.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)

[Get-SPOAppErrors](Get-SPOAppErrors.md)

[Set-SPOGeoStorageQuota](set-SPOGeoStorageQuota.md)
