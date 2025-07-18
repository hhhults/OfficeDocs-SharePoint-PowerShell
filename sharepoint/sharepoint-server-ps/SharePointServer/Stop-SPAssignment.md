---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/stop-spassignment
applicable: SharePoint Server Subscription Edition
title: Stop-SPAssignment
schema: 2.0.0
---

# Stop-SPAssignment

## SYNOPSIS
Disposes of objects in the provided assignment collection.

## SYNTAX

```
Stop-SPAssignment [[-SemiGlobal] <SPAssignmentCollection>] [-AssignmentCollection <SPAssignmentCollection>]
 [-Global] [<CommonParameters>]
```

## DESCRIPTION
The `Stop-SPAssignment` cmdlet disposes of objects in the provided assignment collection.
Use the Global parameter to dispose of all objects in the global assignment collector and to stop the global store from collecting additional objects.
Provide a SemiGlobal assignment collector to dispose of all contained objects.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
Start-SPAssignment -global
$w = Get-SPWeb https://MyWeb
$w | Set-SPWeb -title "Accounting"
Stop-SPAssignment -global
```

This example uses simple assignment.
While easier to use simple assignment, running commands that iterate through multiple SPSite or SPWeb objects while simple assignment is enabled is not recommended.
Ensure that `Stop-SPAssignment` is run before attempting any iterations of multiple objects.

## PARAMETERS

### -SemiGlobal

> Applicable: SharePoint Server Subscription Edition

Provides the assignment collector from which to dispose of objects.

```yaml
Type: SPAssignmentCollection
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
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

### -Global

> Applicable: SharePoint Server Subscription Edition

Stops the global assignment collector from storing objects and disposes of any objects contained by the global assignment collector.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

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
