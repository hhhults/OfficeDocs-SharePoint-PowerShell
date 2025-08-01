---
external help file: Microsoft.Office.Word.Server.dll-Help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/remove-spwordconversionservicejobhistory
applicable: SharePoint Server Subscription Edition
title: Remove-SPWordConversionServiceJobHistory
schema: 2.0.0
---

# Remove-SPWordConversionServiceJobHistory

## SYNOPSIS
Removes entries from the Word Automation Services job history database.

## SYNTAX

```
Remove-SPWordConversionServiceJobHistory [-Identity] <WordServiceApplicationPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-BeforeDate <DateTime>] [-Confirm] [-IncludeActiveJobs]
 [-JobId <Guid>] [-SubscriptionId <Guid>] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
The `Remove-SPWordConversionServiceJobHistory` cmdlet removes entries from the Word Automation Services job history database.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE 1
```powershell
Get-SPServiceApplication -Name TestWordServer | Remove-SPWordConversionServiceJobHistory -BeforeDate 1/1/2009
```

This example deletes all the items in the database before 1/1/2009.

### EXAMPLE 2
```powershell
Get-SPServiceApplication -Name TestWordServer | Remove-SPWordConversionServiceJobHistory -JobId 00000000-0000-0112-08FF-63927635FEF1 -IncludeActiveJobs
```

This example deletes the job with the specified ID, even if it is still processing.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the Word Automation Services application to be processed.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a Word Automation Services application (for example, WordSvcApp1); or an instance of a valid SPServiceApplication object.

```yaml
Type: WordServiceApplicationPipeBind
Parameter Sets: (All)
Aliases:

Required: True
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

### -BeforeDate

> Applicable: SharePoint Server Subscription Edition

Specifies that only jobs started before this date are to be removed.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -IncludeActiveJobs

> Applicable: SharePoint Server Subscription Edition

Specifies that jobs that contain active conversions can be removed.
By default, jobs that have active conversions are not removed.

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

### -JobId

> Applicable: SharePoint Server Subscription Edition

Specifies that only the job with the specified ID is to be removed.

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

### -SubscriptionId

> Applicable: SharePoint Server Subscription Edition

Specifies that only jobs corresponding to this subscription ID are to be removed.

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
