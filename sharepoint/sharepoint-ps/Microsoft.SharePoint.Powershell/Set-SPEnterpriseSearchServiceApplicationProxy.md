---
external help file: Microsoft.Office.Server.Search.dll-help.xml
Module Name: Microsoft.SharePoint.Powershell
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-spenterprisesearchserviceapplicationproxy
applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019
title: Set-SPEnterpriseSearchServiceApplicationProxy
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# Set-SPEnterpriseSearchServiceApplicationProxy

## SYNOPSIS
Sets properties of a search service application proxy.

## SYNTAX

```
Set-SPEnterpriseSearchServiceApplicationProxy [-Identity] <SearchServiceApplicationProxyPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-Name <String>] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet updates properties of a site administration service application proxy for a search application.
SPEnterpriseSearchServiceApplicationProxy represents the proxy for search site administration functionality.
One search service application proxy exists for each search application on a farm.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```
Get-SPEnterpriseSearchServiceApplicationProxy -Identity SsaProxy | Set- SPEnterpriseSearchServiceApplicationProxy -Name ContosoSearchProxy
```

This example sets the display name of a search service application proxy.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specified the search service application proxy to update.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a search service application proxy (for example, SearchServiceAppProxy1); or an instance of a valid SearchServiceApplicationProxy object.

```yaml
Type: SearchServiceApplicationProxyPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AssignmentCollection

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Manages objects for the purpose of proper disposal.
Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management.
Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory.
When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

When the Global parameter is used, all objects are contained in the global store.
If objects are not immediately used, or disposed of by using the `Stop-SPAssignment` command, an out-of-memory scenario can occur.

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

### -Confirm

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Prompts you for confirmation before executing the command.
For more information, type the following command: `get-help about_commonparameters`

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the display name of the search application proxy to retrieve.

The type must be a valid string, for example, SearchAppProxy1.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Displays a message that describes the effect of the command instead of executing the command.
For more information, type the following command: `get-help about_commonparameters`

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
