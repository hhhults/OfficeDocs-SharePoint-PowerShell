---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-spserviceapplication
applicable: SharePoint Server Subscription Edition
title: Set-SPServiceApplication
schema: 2.0.0
---

# Set-SPServiceApplication

## SYNOPSIS
Sets properties of a service application.

## SYNTAX

```
Set-SPServiceApplication [-Identity] <SPServiceApplicationPipeBind>
 [-DefaultEndpoint <SPServiceEndpointPipeBind>] [-AssignmentCollection <SPAssignmentCollection>]
 [-IisWebServiceApplicationPool <SPIisWebServiceApplicationPoolPipeBind>]
 [-ServiceApplicationProxyGroup <SPServiceApplicationProxyGroupPipeBind>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## DESCRIPTION
Use the `Set-SPServiceApplication` cmdlet to set various properties of a service application such as the default endpoint and the application pool used by the service application.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
$serviceapp = Get-SPServiceApplication "My Service App"
Set-SPServiceApplication $serviceapp -DefaultEndpoint https
```

This example sets the default endpoint of the service application to be https.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the service application to update.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a subscription settings service application (for example, SubSettingsApp1); or an instance of a valid SPServiceApplication object.

```yaml
Type: SPServiceApplicationPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultEndpoint

> Applicable: SharePoint Server Subscription Edition

Specifies the address of the default endpoint of the service application.

```yaml
Type: SPServiceEndpointPipeBind
Parameter Sets: (All)
Aliases:

Required: False
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

### -IisWebServiceApplicationPool

> Applicable: SharePoint Server Subscription Edition

Specifies the name or identity of the application pool used by the service application.

The IisWebServiceApplicationPool parameter only applies to Web Service applications.

```yaml
Type: SPIisWebServiceApplicationPoolPipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceApplicationProxyGroup

> Applicable: SharePoint Server Subscription Edition

Specifies a custom service application proxy group for the Web application to use.
The Web application will use the proxies in this proxy group to connect to service applications.
If the ServiceApplicationProxyGroup parameter is not specified, the farm's default proxy group is used.

```yaml
Type: SPServiceApplicationProxyGroupPipeBind
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
