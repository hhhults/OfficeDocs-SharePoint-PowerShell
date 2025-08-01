---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/start-spservice

title: Start-SPService
schema: 2.0.0
---

# Start-SPService

## SYNOPSIS
Enables a service in the farm.

## SYNTAX

```
Start-SPService [-Identity] <SPServicePipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 [-IncludeCustomServerRole] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
The Start-SPService cmdlet enables a service in the farm. Service instances for this service will be started on the appropriate servers in the farm.

This cmdlet only controls service instances on servers that are managed by MinRole. The behavior for the Custom server role has changed with the November 2016 Public Update (PU). Please see the IncludeCustomServerRole parameter for additional information.

## EXAMPLES

### EXAMPLE
```powershell
Start-SPService -Identity "Microsoft SharePoint Foundation Sandboxed Code Service"
```

This example enables the Microsoft SharePoint Foundation Sandboxed Code Service in the farm.

## PARAMETERS

### -AssignmentCollection

> Applicable: SharePoint Server Subscription Edition

Manages objects for the purpose of proper disposal. Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

When the Global parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the Stop-SPAssignment command, an out-of-memory scenario can occur.

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

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the service to enable.

```yaml
Type: SPServicePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IncludeCustomServerRole

> Applicable: SharePoint Server Subscription Edition

Creates a timer job that also starts service instances on servers that are assigned to the custom server role.

This is a one-time Timer job. MinRole will make no further attempts to manage the service instances on servers assigned to the Custom server role.

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

### Microsoft.SharePoint.PowerShell.SPServicePipeBind
Microsoft.SharePoint.PowerShell.SPAssignmentCollection

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
