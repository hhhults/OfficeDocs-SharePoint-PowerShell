---
external help file: Microsoft.Office.Server.Search.dll-help.xml
Module Name: Microsoft.SharePoint.Powershell
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/new-spenterprisesearchadmincomponent
applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019
title: New-SPEnterpriseSearchAdminComponent
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# New-SPEnterpriseSearchAdminComponent

## SYNOPSIS
Creates a new admin component for the given topology and search service instance.

## SYNTAX

```
New-SPEnterpriseSearchAdminComponent -SearchServiceInstance <SearchServiceInstancePipeBind>
 -SearchTopology <SearchTopologyPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 [-SearchApplication <SearchServiceApplicationPipeBind>] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
Creates a new search admin component and adds it to an inactive search topology in a specific search service instance.
The change is effectuated when the search topology is enabled.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```
$si = Get-SPEnterpriseSearchServiceInstance
$ssa = Get-SPEnterpriseSearchServiceApplication
$topology = Get-SPEnterpriseSearchTopology -SearchApplication $ssa
New-SPEnterpriseSearchAdminComponent -SearchTopology $topology -SearchServiceInstance $si -SearchApplication $ssa
```

This example adds a new Search Administration Component to the inactive topology for the existing Search Service Application.

## PARAMETERS

### -SearchServiceInstance

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the search service instance that will host the new admin component.

```yaml
Type: SearchServiceInstancePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchTopology

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the search topology where the new admin component should be added.

```yaml
Type: SearchTopologyPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
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

### -SearchApplication

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the search service application that contains the search topology.

```yaml
Type: SearchServiceApplicationPipeBind
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
