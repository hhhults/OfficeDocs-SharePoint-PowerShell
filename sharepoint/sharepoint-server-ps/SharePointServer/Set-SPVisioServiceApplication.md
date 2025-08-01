---
external help file: Microsoft.Office.Visio.Server.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-spvisioserviceapplication
applicable: SharePoint Server Subscription Edition
title: Set-SPVisioServiceApplication
schema: 2.0.0
---

# Set-SPVisioServiceApplication

## SYNOPSIS
Sets the ServiceApplicationPool property for a Visio Services application.

## SYNTAX

```
Set-SPVisioServiceApplication [-Identity] <SPVisioServiceApplicationPipeBind>
 [-ServiceApplicationPool] <SPIisWebServiceApplicationPoolPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
The `Set-SPVisioServiceApplication` cmdlet sets the ServiceApplicationPool property for a Visio Services application.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE 1
```powershell
Set-SPVisioServiceApplication -identity "VGS1" -ServiceApplicationPool "SharePoint Web Services System Default"
```

This example changes the application pool of the VGS1 service application.

### EXAMPLE 2
```powershell
Get-SPServiceApplicationPool "SharePoint Web Services Default" | Set-SPVisioServiceApplication VGS1
```

This example changes the application pool of the VGS1 service application.
The results are piped from the `Get-SPServiceApplicationPool` cmdlet.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the Visio Services application to update.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a Visio Services application (for example, MyVisioService1); or an instance of a valid SPVisioServiceApplication object.

```yaml
Type: SPVisioServiceApplicationPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ServiceApplicationPool

> Applicable: SharePoint Server Subscription Edition

Specifies the IIS application pool to change.
The Web service for the service application runs in the specified application pool.

The type must be a valid name of a Visio Service application pool, such as MyVisioServiceAppPool1; or a valid GUID, such as 12345678-90ab-cdef-1234-567890bcdefgh, or an instance of a valid SPIisWebServiceApplicationPoolPipeBind object.

```yaml
Type: SPIisWebServiceApplicationPoolPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
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
