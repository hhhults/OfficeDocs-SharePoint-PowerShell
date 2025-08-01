---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-spusagedefinition
applicable: SharePoint Server Subscription Edition
title: Set-SPUsageDefinition
schema: 2.0.0
---

# Set-SPUsageDefinition

## SYNOPSIS
Sets the retention period for a usage provider.

## SYNTAX

```
Set-SPUsageDefinition [-Identity] <SPUsageDefinitionPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
 [-Confirm] [-DaysRetained <Int32>] [-DaysToKeepUsageFiles <Int32>] [-Enable] [-MaxTotalSizeInBytes <Int64>]
 [-WhatIf] [-UsageDatabaseEnabled] [<CommonParameters>]
```

## DESCRIPTION
The `Set-SPUsageDefinition` cmdlet sets the retention period for a specified usage provider.
A usage definition object defines a specific type of usage provider.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
Set-SPUsageDefinition -Identity "Page Requests" -DaysRetained 31
```

This example sets the number of days that stores page requests usage data to 31.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the usage definition object to update.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a usage definition (for example, SiteSubscriptionConfig1); or an instance of a valid SPUsageDefinition object.

```yaml
Type: SPUsageDefinitionPipeBind
Parameter Sets: (All)
Aliases:

Required: True
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

### -DaysRetained

> Applicable: SharePoint Server Subscription Edition

Specifies the number of days that usage data for the usage provider is retained in the usage service database.
The default value is 14.

The type must be an integer between 0 and 31.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DaysToKeepUsageFiles

> Applicable: SharePoint Server Subscription Edition

Specifies the number of days to keep usage file retention.
The value must be less than or equal to value of the DaysRetained parameter.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enable

> Applicable: SharePoint Server Subscription Edition

Turns on the specified usage provider.

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

### -MaxTotalSizeInBytes

> Applicable: SharePoint Server Subscription Edition

This parameter stores the maximum SQL storage size for the data of this provider.

```yaml
Type: Int64
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

### -UsageDatabaseEnabled

> Applicable: SharePoint Server Subscription Edition

Set to export usage data from the local server to the Usage database.

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
