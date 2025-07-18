---
external help file: Microsoft.Office.Server.Search.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/new-spenterprisesearchindexcomponent
applicable: SharePoint Server Subscription Edition
title: New-SPEnterpriseSearchIndexComponent
schema: 2.0.0
---

# New-SPEnterpriseSearchIndexComponent

## SYNOPSIS
Creates a new index component for the given topology and search service instance.

## SYNTAX

```
New-SPEnterpriseSearchIndexComponent -SearchServiceInstance <SearchServiceInstancePipeBind>
 -SearchTopology <SearchTopologyPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 [-IndexPartition <UInt32>] [-RootDirectory <String>] [-SearchApplication <SearchServiceApplicationPipeBind>]
 [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
Creates a new index component and adds it to an inactive search topology in a specific search service instance.
The change is effectuated when the search topology is enabled.

## EXAMPLES

### EXAMPLE
```powershell
$si = Get-SPEnterpriseSearchServiceInstance
$ssa = Get-SPEnterpriseSearchServiceApplication
$topology = Get-SPEnterpriseSearchTopology -SearchApplication $ssa
New-SPEnterpriseSearchIndexComponent -SearchTopology $topology -SearchServiceInstance $si -SearchApplication $ssa -IndexPartition 1 -RootDirectory E:\Index
```

This example adds a new Search Index Component to the inactive topology for the existing Search Service Application. The directory of the Index Component is set to E:\Index with a Partition number of 1.

## PARAMETERS

### -SearchServiceInstance

> Applicable: SharePoint Server Subscription Edition

Specifies the search service instance that will host the new index component.

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

> Applicable: SharePoint Server Subscription Edition

Specifies the search topology where the new index component should be added.

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

> Applicable: SharePoint Server Subscription Edition

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

> Applicable: SharePoint Server Subscription Edition

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

### -IndexPartition

> Applicable: SharePoint Server Subscription Edition

Specifies the index partition number to assign to the new search index component.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RootDirectory

> Applicable: SharePoint Server Subscription Edition

Specifies the root directory that will hold the index location for the new search index component.
This is needed if you want to isolate the index on dedicated discs in order to avoid I/O contention with other parts of the system, other system sharing the same disks, or because you do not want to risk the index filling up the OS disk (generally C: )

If you specify the root directory to be the root of a volume, e.g.
E:, the index will not be cleaned up if you delete the SSA.
You will then have to delete the SSA manually.

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

### -SearchApplication

> Applicable: SharePoint Server Subscription Edition

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

> Applicable: SharePoint Server Subscription Edition

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
