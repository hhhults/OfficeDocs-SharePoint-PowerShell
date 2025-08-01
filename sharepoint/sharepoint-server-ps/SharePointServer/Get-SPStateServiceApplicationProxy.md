---
external help file: Microsoft.Office.Server.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/get-spstateserviceapplicationproxy
applicable: SharePoint Server Subscription Edition
title: Get-SPStateServiceApplicationProxy
schema: 2.0.0
---

# Get-SPStateServiceApplicationProxy

## SYNOPSIS
Returns state service application proxies on the farm.

## SYNTAX

```
Get-SPStateServiceApplicationProxy [[-Identity] <SPStateServiceApplicationProxyPipeBind>]
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
The Get-SPStateServiceApplicationProxy cmdlet returns a state service application proxy on the farm.
If the Identity parameter is not specified, this cmdlet returns the collection of all state service application proxies on the farm.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE 1
```powershell
Get-SPStateServiceApplicationProxy
```

This example displays all the state service application proxies on the farm.

### EXAMPLE 2
```powershell
Get-SPStateServiceApplicationProxy -Identity 81dc50e0-c0f9-4d2c-8284-bb03bb1ea676
```

This example displays a specific state service application proxy on the farm.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the state service application proxy to get.

The type must be a valid name of a state service application proxy (for example, StateServiceProxy); a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh.

```yaml
Type: SPStateServiceApplicationProxyPipeBind
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -AssignmentCollection

> Applicable: SharePoint Server Subscription Edition

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
