---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/restart-spappinstancejob
applicable: SharePoint Server Subscription Edition
title: Restart-SPAppInstanceJob
schema: 2.0.0
---

# Restart-SPAppInstanceJob

## SYNOPSIS
Restarts an app instance.

## SYNTAX

```
Restart-SPAppInstanceJob -AppInstance <SPAppInstance> [-AssignmentCollection <SPAssignmentCollection>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
Use the Restart-SPAppInstanceJob cmdlet to restart an app instance.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at Windows PowerShell for SharePoint Server 2016, SharePoint Server 2019 reference (https://go.microsoft.com/fwlink/p/?LinkId=671715).

## EXAMPLES

### EXAMPLE
```powershell
$instance = Get-SPAppInstance -Web https://site_url | ?{$_.Title -eq 'Contoso App'}
Restart-SPAppInstanceJob -AppInstance $instance
```

Restarts the App Instance for the App named 'Contoso App' on https://site_url.

## PARAMETERS

### -AppInstance

> Applicable: SharePoint Server Subscription Edition

Specifies the app instance object to restart.

```yaml
Type: SPAppInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

Prompts you for confirmation before running the cmdlet.

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

Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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

### Microsoft.SharePoint.PowerShell.SPAssignmentCollection

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
