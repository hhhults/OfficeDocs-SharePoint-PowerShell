---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/add-sproutingmachinepool
applicable: SharePoint Server Subscription Edition
title: Add-SPRoutingMachinePool
schema: 2.0.0
---

# Add-SPRoutingMachinePool

## SYNOPSIS

Adds a new machine pool.


## SYNTAX

```
Add-SPRoutingMachinePool [-RequestManagementSettings] <SPRequestManagementSettingsPipeBind> [-Name] <String>
 [-AssignmentCollection <SPAssignmentCollection>] [-MachineTargets <SPRoutingRuleTargetPipeBind[]>]
 [<CommonParameters>]
```

## DESCRIPTION
Use the Add-SPRoutingMachinePool cmdlet to add a machine pool by using the RequestManagementSettings and Name parameters.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
$web=Get-SPWebApplication -Identity <URL of web application>
$rm=Get-SPRequestManagementSettings -Identity $web
Add-SPRoutingMachinePool -RequestManagementSettings $rm -Name <MachineName>
```

This example adds a machine pool.

## PARAMETERS

### -RequestManagementSettings

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the request management settings object to add to the routing machine pool.

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

### -Name

> Applicable: SharePoint Server Subscription Edition

Specifies the name of machine pool.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
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
If objects are not immediately used, or disposed of by using the Stop-SPAssignment command, an out-of-memory scenario can occur.

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

### -MachineTargets

> Applicable: SharePoint Server Subscription Edition

Specifies the routing targets collection that the machine pool will contain.

```yaml
Type: SPRoutingRuleTargetPipeBind[]
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

[Get-SPRoutingMachinePool](Get-SPRoutingMachinePool.md)

[Remove-SPRoutingMachinePool](Remove-SPRoutingMachinePool.md)

[Set-SPRoutingMachinePool](Set-SPRoutingMachinePool.md)
