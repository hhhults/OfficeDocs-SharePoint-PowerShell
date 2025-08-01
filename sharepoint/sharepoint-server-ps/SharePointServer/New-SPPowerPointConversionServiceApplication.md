---
external help file: Microsoft.Office.Server.Powerpoint.dll-Help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/new-sppowerpointconversionserviceapplication
applicable: SharePoint Server Subscription Edition
title: New-SPPowerPointConversionServiceApplication
schema: 2.0.0
---

# New-SPPowerPointConversionServiceApplication

## SYNOPSIS
Creates a PowerPoint Conversion Service application.

## SYNTAX

```
New-SPPowerPointConversionServiceApplication [-Name] <String>
 -ApplicationPool <SPIisWebServiceApplicationPoolPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
Use the `New-SPPowerPointConversionServiceApplication` cmdlet to create a new instance of a PowerPoint Conversion Service application by using the Name parameter.

After the PowerPoint Conversion Service application is created, you can convert PowerPoint presentations to various formats.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### Example
```powershell
New-SPPowerPointConversionServiceApplication -Name "PowerPoint Conversion Service Application" -ApplicationPool "SharePoint Web Services Default"
```

This example creates a new instance of the PowerPoint Conversion Service application named _PowerPoint Conversion Service Application_ and assigns it to the default application pool.

## PARAMETERS

### -Name

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the PowerPoint Conversion Service application.

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

### -ApplicationPool

> Applicable: SharePoint Server Subscription Edition

Assigns an application pool that Internet Information Services (IIS) will use for this service application.

```yaml
Type: SPIisWebServiceApplicationPoolPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
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

[New-SPPowerPointConversionServiceApplicationProxy](New-SPPowerPointConversionServiceApplicationProxy.md)

[Set-SPPowerPointConversionServiceApplication](Set-SPPowerPointConversionServiceApplication.md)
