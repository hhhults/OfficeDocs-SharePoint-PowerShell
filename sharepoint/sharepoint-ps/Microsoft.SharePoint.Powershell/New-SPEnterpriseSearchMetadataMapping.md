---
external help file: Microsoft.Office.Server.Search.dll-help.xml
Module Name: Microsoft.SharePoint.Powershell
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/new-spenterprisesearchmetadatamapping
applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019
title: New-SPEnterpriseSearchMetadataMapping
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# New-SPEnterpriseSearchMetadataMapping

## SYNOPSIS
Adds a managed property mapping.

## SYNTAX

```
New-SPEnterpriseSearchMetadataMapping -CrawledProperty <CrawledPropertyPipeBind>
 -ManagedProperty <ManagedPropertyPipeBind> -SearchApplication <SearchServiceApplicationPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-SiteCollection <Guid>] [-Tenant <Guid>]
 [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet maps a crawled property to a managed property.
SPEnterpriseSearchMetadataMapping represents a snapshot of a mapping between a managed property and one or more crawled properties in the enterprise search metadata property schema.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```
$ssa = Get-SPEnterpriseSearchServiceApplication
$mp = Get-SPEnterpriseSearchMetadataManagedProperty -SearchApplication $ssa -Identity UserName
$cat = Get-SPEnterpriseSearchMetadataCategory -SearchApplication $ssa -Identity People
$cp = Get-SPEnterpriseSearchMetadataCrawledProperty -SearchApplication $ssa -Category $cat -Limit 1
$ncp = New-SPEnterpriseSearchMetadataCrawledProperty -SearchApplication $ssa -Name "MyCrawlProp" -PropSet $cp.PropSet -Category $cp.CategoryName -IsNameEnum $false -VariantType $cp.VariantType -IsMappedToContents $true
New-SPEnterpriseSearchMetadataMapping -SearchApplication $ssa -ManagedProperty $mp -CrawledProperty $ncp
```

This example maps the created crawled property MyCrawlProp to the managed property UserName for the default search service application.

The VarientType parameter is marked as obsolete but is still required when executing the `New-SPEnterpriseSearchMetadataCrawledProperty` cmdlet.

## PARAMETERS

### -CrawledProperty

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the crawled property to map.

The type must be a valid GUID in the form 12345678-90ab-cdef-1234-567890bcdefgh, a valid URL in the form https://server_name, or an instance of a valid CrawledProperty object.

```yaml
Type: CrawledPropertyPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedProperty

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the managed property to which the crawled property should be mapped.

The type must be a valid GUID in the form 12345678-90ab-cdef-1234-567890bcdefgh, a valid name of a managed property, for example, ManagedProperty1, or an instance of a valid ManagedProperty object.

```yaml
Type: ManagedPropertyPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchApplication

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the search application that contains the metadata mapping.

The type must be a valid search application name, for example, SearchApp1, or an instance of a valid SearchServiceApplication object.

```yaml
Type: SearchServiceApplicationPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AssignmentCollection

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

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

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

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

### -SiteCollection

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies that the metadata mapping returned are to be within the scope of a site collection (SPSite).

The type must be a valid GUID that specifies the property set in the form 12345678-90ab-cdef-1234-567890bcdefgh.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tenant

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies that the metadata mapping returned are to be within the scope of a tenant.

The type must be a valid GUID that specifies the property set in the form 12345678-90ab-cdef-1234-567890bcdefgh.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

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
