---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/get-spavailabilitygroupstatus
applicable: SharePoint Server Subscription Edition
title: Get-SPAvailabilityGroupStatus
schema: 2.0.0
---

# Get-SPAvailabilityGroupStatus

## SYNOPSIS
Returns one or more objects representing the availability groups known to the SharePoint farm.

## SYNTAX

```
Get-SPAvailabilityGroupStatus [-AssignmentCollection <SPAssignmentCollection>] [-Identity <String>]
 [<CommonParameters>]
```

## DESCRIPTION
Returns one or more objects representing the availability groups known to the SharePoint farm.

## EXAMPLES

### Example 1
```powershell
Get-SPAvailabilityGroupStatus -Identity MyAvailabilityGroup
```

This example returns an availability group named "MyAvailabilityGroup".

## PARAMETERS

### -AssignmentCollection

> Applicable: SharePoint Server Subscription Edition

Manages objects for the purpose of proper disposal. Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

NOTE: When the Global parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the Stop-SPAssignment command, an out-of-memory scenario can occur.

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

### -Identity

> Applicable: SharePoint Server Subscription Edition

Finds the availability group whose name property matches this string. Otherwise, returns all availability groups.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.SharePoint.PowerShell.SPAssignmentCollection

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
