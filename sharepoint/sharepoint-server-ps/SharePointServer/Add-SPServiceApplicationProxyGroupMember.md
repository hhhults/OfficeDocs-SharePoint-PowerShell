---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/add-spserviceapplicationproxygroupmember
applicable: SharePoint Server Subscription Edition
title: Add-SPServiceApplicationProxyGroupMember
schema: 2.0.0
---

# Add-SPServiceApplicationProxyGroupMember

## SYNOPSIS

Adds a member to the service application proxy group.


## SYNTAX

```
Add-SPServiceApplicationProxyGroupMember [-Identity] <SPServiceApplicationProxyGroupPipeBind>
 [-Member] <SPServiceApplicationProxyPipeBind[]> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
The Add-SPServiceApplicationProxyGroupMember cmdlet adds a member to the service application proxy group.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
$proxy = Get-SPServiceApplicationProxy | ?{$_.TypeName -match 'User Profile Service Application Proxy'}
Add-SPServiceApplicationProxyGroupMember RemoteProxyGroup -Member $proxy
```

This example adds a select service application proxy to the service application proxy group named RemoteProxyGroup.

The service application proxy group GUID is unique to every farm.
You can run Get-SPServiceApplicationProxyGroup | Select Name,Id to see the GUID of the serviceapplication proxy groups.
Use this result for any other SPServiceApplicationProxyGroup cmdlets.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the service application proxy group to which to add the member.

```yaml
Type: SPServiceApplicationProxyGroupPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Member

> Applicable: SharePoint Server Subscription Edition

Specifies an array of members to add to the service application proxy group.

```yaml
Type: SPServiceApplicationProxyPipeBind[]
Parameter Sets: (All)
Aliases: Proxy

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
