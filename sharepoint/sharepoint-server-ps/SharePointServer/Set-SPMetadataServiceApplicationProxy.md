---
external help file: Microsoft.SharePoint.Taxonomy.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-spmetadataserviceapplicationproxy
applicable: SharePoint Server Subscription Edition
title: Set-SPMetadataServiceApplicationProxy
schema: 2.0.0
---

# Set-SPMetadataServiceApplicationProxy

## SYNOPSIS
Sets the properties of a connection to a managed metadata service application.

## SYNTAX

```
Set-SPMetadataServiceApplicationProxy [-Identity] <SPMetadataServiceProxyCmdletPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-ContentTypePushdownEnabled]
 [-ContentTypeSyndicationEnabled] [-DefaultKeywordTaxonomy] [-DefaultSiteCollectionTaxonomy] [-Name <String>]
 [-DefaultProxyGroup] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
Use the `Set-SPMetadataServiceApplicationProxy` cmdlet to set the properties of a connection to a managed metadata service application.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE 1
```powershell
Set-SPMetadataServiceApplicationProxy -Identity "MetadataServiceProxy1" -ContentTypeSyndicationEnabled -ContentTypePushdownEnabled
```

This example enables content type syndication and enables content type pushdown on an existing connection to a managed metadata service application.

### EXAMPLE 2
```powershell
Set-SPMetadataServiceApplicationProxy -Identity "MetadataServiceProxy1" -ContentTypeSyndicationEnabled:$false -ContentTypePushdownEnabled:$false
```

This example disables content type syndication and disables content type pushdown on an existing connection to a managed metadata service application.

### EXAMPLE 3
```powershell
Set-SPMetadataServiceApplicationProxy -Identity "MetadataServiceProxy1" -DefaultKeywordTaxonomy -DefaultSiteCollectionTaxonomy:$false
```

This example configures an existing connection to a managed metadata service application to be the default location for storing enterprise keywords and prevents it from being the default location for storing column-specific term sets.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the connection to update.

The type must be a GUID that represents the identity of the connection to modify, the name of a valid connection to a managed metadata service, or an instance of a valid SPMetadataServiceProxy object.

```yaml
Type: SPMetadataServiceProxyCmdletPipeBind
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

### -ContentTypePushdownEnabled

> Applicable: SharePoint Server Subscription Edition

Specifies that existing instances of changed content types in subsites and libraries will be updated.

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

### -ContentTypeSyndicationEnabled

> Applicable: SharePoint Server Subscription Edition

Specifies that this connection will provide access to the content types that are associated with the managed metadata service application.

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

### -DefaultKeywordTaxonomy

> Applicable: SharePoint Server Subscription Edition

Specifies that new enterprise keywords will be stored in the term store associated with the managed metadata service application.

Do not make more than one connection the default keyword location.

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

### -DefaultSiteCollectionTaxonomy

> Applicable: SharePoint Server Subscription Edition

Specifies that the term set that is created when you create a new managed metadata column will be stored in the term store associated with the managed metadata service application.

Do not make more than one connection the default location for site collection term sets.

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

### -Name

> Applicable: SharePoint Server Subscription Edition

Specifies the new display name of the connection.
The name can contain a maximum of 128 characters.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProxyGroup

> Applicable: SharePoint Server Subscription Edition

Specifies that the connection be added to the default proxy group of the farm.

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
