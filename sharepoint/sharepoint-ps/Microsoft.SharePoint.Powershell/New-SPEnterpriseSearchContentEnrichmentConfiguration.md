---
external help file: Microsoft.Office.Server.Search.dll-help.xml
Module Name: Microsoft.SharePoint.Powershell
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/new-spenterprisesearchcontentenrichmentconfiguration
applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019
title: New-SPEnterpriseSearchContentEnrichmentConfiguration
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# New-SPEnterpriseSearchContentEnrichmentConfiguration

## SYNOPSIS
Creates a new ContentEnrichmentConfiguration object.

## SYNTAX

```
New-SPEnterpriseSearchContentEnrichmentConfiguration [-AssignmentCollection <SPAssignmentCollection>]
 [<CommonParameters>]
```

## DESCRIPTION
This cmdlet creates a new ContentEnrichmentConfiguration object that the user can change.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```
C:\PS>$config = New-SPEnterpriseSearchContentEnrichmentConfiguration
```

This example creates a new ContentEnrichmentConfiguration object.

## PARAMETERS

### -AssignmentCollection

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Manages objects for the purpose of proper disposal.
Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management.
Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory.
When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

When the Global parameter is used, all objects are contained in the global store.
If objects are not immediately used, or disposed of by using the Stop-SPAssignment command, an out-of-memory scenario can occur.

```yaml
Type: SPAssignmentCollection
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-SPEnterpriseSearchContentEnrichmentConfiguration](Get-SPEnterpriseSearchContentEnrichmentConfiguration.md)

[Set-SPEnterpriseSearchContentEnrichmentConfiguration](Set-SPEnterpriseSearchContentEnrichmentConfiguration.md)

[Remove-SPEnterpriseSearchContentEnrichmentConfiguration](Remove-SPEnterpriseSearchContentEnrichmentConfiguration.md)
