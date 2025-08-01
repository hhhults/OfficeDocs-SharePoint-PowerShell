---
external help file: Microsoft.Office.Server.Search.dll-help.xml
Module Name: Microsoft.SharePoint.Powershell
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/move-spenterprisesearchlinksdatabases
applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019
title: Move-SPEnterpriseSearchLinksDatabases
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# Move-SPEnterpriseSearchLinksDatabases

## SYNOPSIS
Moves data across links databases.

## SYNTAX

```
Move-SPEnterpriseSearchLinksDatabases [-SearchApplication] <SearchServiceApplicationPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-RepartitioningId <Guid>]
 [-SourceStores <LinksStore[]>] [-TargetStores <LinksStore[]>] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
The Move-SPEnterpriseSearchLinksDatabases cmdlet moves data across a given list of links databases during farm configuration and scale out, to improve the performance and resource load of the farm.
Once the move has started, the cmdlet will return a unique identifier, the RepartitioningId.
Use this identifier to retrigger if the current run fails.
After the move has finished, the old databases can be removed.

A links database stores query logging and analytics information.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```
$ssa = Get-SPEnterpriseSearchServiceapplication
$ssa | New-SPEnterpriseSearchLinksDatabase -DatabaseName "links1"
$ssa | New-SPEnterpriseSearchLinksDatabase -DatabaseName "links2"
$ssa | New-SPEnterpriseSearchLinksDatabase -DatabaseName "links3"
$dbs = $ssa | Get-SPEnterpriseSearchLinksDatabase
$ssa | Move-SPEnterpriseSearchLinksDatabases -TargetStores $dbs
```

This example adds 3 new links databases and uses Move-SPEnterpriseSearchLinksDatabases to move data from the current links databases into new databases.

## PARAMETERS

### -SearchApplication

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the search application that contains the links database.
The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid SearchServiceApplication object.

Specifies the search application that contains the links database.
The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid SearchServiceApplication object.


```yaml
Type: SearchServiceApplicationPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

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

### -Confirm

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

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

### -RepartitioningId

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Resumes the move with this identifier.


```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceStores

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies a source list of databases.
If this parameter is not specified then all currently existing links databases will be used as a source list.


```yaml
Type: LinksStore[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetStores

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies a target list of databases.
If this parameter is not specified then all currently existing links databases will be used as a target list.


```yaml
Type: LinksStore[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216 (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-SPEnterpriseSearchLinksDatabase](New-SPEnterpriseSearchLinksDatabase.md)

[Set-SPEnterpriseSearchLinksDatabase](Set-SPEnterpriseSearchLinksDatabase.md)

[Get-SPEnterpriseSearchLinksDatabase](Get-SPEnterpriseSearchLinksDatabase.md)

[Remove-SPEnterpriseSearchLinksDatabase](Remove-SPEnterpriseSearchLinksDatabase.md)
