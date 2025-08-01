---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: Microsoft.SharePoint.Powershell
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-sprequestmanagementsettings
applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019
title: Set-SPRequestManagementSettings
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# Set-SPRequestManagementSettings

## SYNOPSIS
Sets Request Manager properties.

## SYNTAX

```
Set-SPRequestManagementSettings [-Identity] <SPRequestManagementSettingsPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-RoutingEnabled] [-RoutingScheme <SPRoutingScheme>]
 [-ThrottlingEnabled] [<CommonParameters>]
```

## DESCRIPTION
Use the `Set-SPRequestManagementSettings` cmdlet to set properties for the Request Manager.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```
$wa = Get-SPWebApplication https://webAppUrl
$req = $wa | Get-SPRequestManagementSettings
Set-SPRequestManagementSettings -Identity $req -ThrottlingEnabled:$false
```

This example disables throttling on the specified Web Application.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the Request Manager object for which settings will be applied.

```yaml
Type: SPRequestManagementSettingsPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AssignmentCollection

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

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

### -RoutingEnabled

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies whether routing is enabled or disabled for the Request Manager object.

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

### -RoutingScheme

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the routing scheme.

The value is one of the following:

--Default- Performs random selection.
--StaticMachineWeight- Uses Static weight of target.
--HealthBased- Considers health score of machine.

```yaml
Type: SPRoutingScheme
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThrottlingEnabled

> Applicable: SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies whether throttling is enabled or disabled for the Request Manager object.

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

[Get-SPRequestManagementSettings](Get-SPRequestManagementSettings.md)

[New-SPRequestManagementRuleCriteria](New-SPRequestManagementRuleCriteria.md)
