---
external help file: Microsoft.SharePoint.Taxonomy.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/get-spmetadataserviceapplication
applicable: SharePoint Server Subscription Edition
title: Get-SPMetadataServiceApplication
schema: 2.0.0
---

# Get-SPMetadataServiceApplication

## SYNOPSIS
Returns a managed metadata service application.

## SYNTAX

```
Get-SPMetadataServiceApplication [-Identity] <SPMetadataServiceCmdletPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [<CommonParameters>]
```

## DESCRIPTION
Use the Get-SPMetadataServiceApplication cmdlet to retrieve a specified managed metadata service application.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
Get-SPMetadataServiceApplication -Identity "ManagedMetadataServiceApp1"
```

This example retrieves an existing managed metadata service application.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the managed metadata service application to get.

The type must be a valid GUID or the name of a valid managed metadata service application.

```yaml
Type: SPMetadataServiceCmdletPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
