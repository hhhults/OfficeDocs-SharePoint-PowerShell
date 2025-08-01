---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-sptimerjob
applicable: SharePoint Server Subscription Edition
title: Set-SPTimerJob
schema: 2.0.0
---

# Set-SPTimerJob

## SYNOPSIS
Sets the schedule for running a timer job.

## SYNTAX

```
Set-SPTimerJob [-Identity] <SPTimerJobPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 [-Schedule <String>] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
The `Set-SPTimerJob` cmdlet sets the schedule for running a specified timer job.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
Get-SPTimerJob job-recycle-bin-cleanup | Set-SPTimerJob -Schedule "weekly at sat 5:00"
```

This example sets the schedule to run the job-recylce-bin-cleanup timer job to weekly at sat 5:00.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the timer job to update.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a timer job (for example, TimerJob1); or an instance of a valid SPTimerJob object.

```yaml
Type: SPTimerJobPipeBind
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

### -Schedule

> Applicable: SharePoint Server Subscription Edition

Specifies the schedule for running the timer job.

The type must be a valid SharePoint Timer service (SPTimer) schedule in the form of any one of the following schedules:

- Every 5 minutes between 0 and 59
- Hourly between 0 and 59
- Daily at 15:00:00
- Weekly between Fri 22:00:00 and Sun 06:00:00
- Monthly at 15 15:00:00
- Yearly at Jan 1 15:00:00

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
