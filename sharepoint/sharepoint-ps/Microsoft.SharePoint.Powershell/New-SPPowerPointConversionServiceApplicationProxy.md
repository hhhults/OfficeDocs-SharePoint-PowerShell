---
external help file: Microsoft.Office.Server.Powerpoint.dll-Help.xml
Module Name: Microsoft.SharePoint.Powershell
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/new-sppowerpointconversionserviceapplicationproxy
applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019
title: New-SPPowerPointConversionServiceApplicationProxy
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# New-SPPowerPointConversionServiceApplicationProxy

## SYNOPSIS
Creates a PowerPoint Conversion Service application proxy.

## SYNTAX

```
New-SPPowerPointConversionServiceApplicationProxy [-Name] <String>
 -ServiceApplication <SPPowerPointConversionServiceApplicationPipeBind> [-AddToDefaultGroup]
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
Use the `New-SPPowerPointConversionServiceApplicationProxy` cmdlet to create a PowerPoint Conversion Service application proxy.
The service application proxy is instantiated on the front-end web server and acts as an intermediary between the client computer and the service application back end.

## EXAMPLES

### EXAMPLE
```
New-SPPowerPointConversionServiceApplicationProxy -Name "MyWorkgroupPPTAppProxy" -ServiceApplication "MyWorkgroupPPTApp" -AddtoDefaultGroup
```

This example creates a new instance of the PowerPoint Conversion Service application proxy named MyWorkgroupPPTAppProxy, binds it to the MyWorkgroupPPTApp service application and then adds it to the default service application proxy group

## PARAMETERS

### -Name

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the name of the service application proxy.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceApplication

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the name of the service application to bind.

```yaml
Type: SPPowerPointConversionServiceApplicationPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AddToDefaultGroup

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Adds the newly created proxy to the default service application proxy group.
If not specified, the proxy is not added to a group.

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

### -AssignmentCollection

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

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

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

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

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

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

[New-SPPowerPointConversionServiceApplication](New-SPPowerPointConversionServiceApplication.md)

[Set-SPPowerPointConversionServiceApplication](Set-SPPowerPointConversionServiceApplication.md)
