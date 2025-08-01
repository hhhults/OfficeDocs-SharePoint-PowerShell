---
external help file: sharepointserver.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/get-spenterprisesearchowner
applicable: SharePoint Server Subscription Edition
title: Get-SPEnterpriseSearchOwner
schema: 2.0.0
---

# Get-SPEnterpriseSearchOwner

## SYNOPSIS
Retrieves the search object owner.

## SYNTAX

```
Get-SPEnterpriseSearchOwner [[-Identity] <SearchObjectOwner>] -Level <SearchObjectLevel>
 [-AssignmentCollection <SPAssignmentCollection>] [-SPWeb <SPWebPipeBind>] [<CommonParameters>]
```

## DESCRIPTION
The Get-SPEnterpriseSearchOwner cmdlet retrieves the search object owner.
Get-SPEnterpriseSearchOwner provides scoping context to other cmdlets such as SPEnterpriseSearchResultItemType.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
Get-SPEnterpriseSearchOwner -Level SPSite
```

This example shows how to retrieve the tenant owner of a search object at the SPSite level.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the search object owner to retrieve.

```yaml
Type: SearchObjectOwner
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Level

> Applicable: SharePoint Server Subscription Edition

Specifies whether the owner object resides at the SPWeb, SPSite, SPSite Subscription, or SSA level.

```yaml
Type: SearchObjectLevel
Parameter Sets: (All)
Aliases: l

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

### -SPWeb

> Applicable: SharePoint Server Subscription Edition

Specifies the SPWeb or SPSite in which this object resides.
It is only needed if Level is equal to SPWeb or SPSite.

```yaml
Type: SPWebPipeBind
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
