---
external help file: Microsoft.Office.Server.Search.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/new-spenterprisesearchmetadatamanagedproperty
applicable: SharePoint Server Subscription Edition
title: New-SPEnterpriseSearchMetadataManagedProperty
schema: 2.0.0
---

# New-SPEnterpriseSearchMetadataManagedProperty

## SYNOPSIS
Adds a managed property to a shared search application.

## SYNTAX

```
New-SPEnterpriseSearchMetadataManagedProperty [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 [-DefaultForQueryIndependentRank <UInt32>] [-Description <String>] [-EnabledForQueryIndependentRank <Boolean>]
 [-EnabledForScoping <Boolean>] [-FullTextQueriable <Boolean>] [-IncludeInAlertSignature <Boolean>]
 [-IncludeInMd5 <Boolean>] -Name <String> [-NameNormalized <Boolean>] [-NoWordBreaker <Boolean>]
 [-Queryable <Boolean>] [-RemoveDuplicates <Boolean>] [-RespectPriority <Boolean>] [-Retrievable <Boolean>]
 [-SafeForAnonymous <Boolean>] -SearchApplication <SearchServiceApplicationPipeBind> [-SiteCollection <Guid>]
 [-Tenant <Guid>] -Type <Int32> [-UserFlags <Int16>] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet creates a new managed property.
SPEnterpriseSearchMetadataManagedProperty represents a managed property in the enterprise search metadata property schema.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
$ssa = Get-SPEnterpriseSearchServiceApplication
New-SPEnterpriseSearchMetadataManagedProperty -Name AboutMeUpdate -SearchApplication $ssa -Type 4
```

This example creates a new managed property named AboutMeUpdate in the default search service application and sets it type to DateTime.

## PARAMETERS

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

### -DefaultForQueryIndependentRank

> Applicable: SharePoint Server Subscription Edition

Specifies that the managed property is mandatory when it is used in query-independent rank (relevance).

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: def

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description

> Applicable: SharePoint Server Subscription Edition

Adds a description to the metadata managed property.

The type must be a valid string.

```yaml
Type: String
Parameter Sets: (All)
Aliases: d

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnabledForQueryIndependentRank

> Applicable: SharePoint Server Subscription Edition

Specifies that the managed property is mandatory when it is used in the custom ranking model for the query-independent work of ranking.

The type must be one of the following query-independent ranking features in the custom model XML:

- queryIndependentFeature
- categoryFeature
- languageFeature

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: qir

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnabledForScoping

> Applicable: SharePoint Server Subscription Edition

Specifies that the managed property can be used in a scope definition.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: e

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FullTextQueriable

> Applicable: SharePoint Server Subscription Edition

Specifies that the managed property can be used in enterprise search SQL queries.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: f

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeInAlertSignature

> Applicable: SharePoint Server Subscription Edition

Specifies whether this managed property should be included in the alert signature.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: ia

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeInMd5

> Applicable: SharePoint Server Subscription Edition

Specifies that the managed property is included in the hash used by the crawler to determine whether a document has changed.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: im5

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the new managed property.

The type must be a valid name of a managed property, for example, ManagedProperty1.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NameNormalized

> Applicable: SharePoint Server Subscription Edition

Specifies if the values of the managed property should be normalized, that is, enable to return results independent of letter casing and diacritics used in the query.
If value is set to true, the values are normalized.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: nn

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWordBreaker

> Applicable: SharePoint Server Subscription Edition

Specifies that the values for this managed property are processed by a word breaker.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: nw

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Queryable

> Applicable: SharePoint Server Subscription Edition

Specifies whether this managed property is queryable or not.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: q

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveDuplicates

> Applicable: SharePoint Server Subscription Edition

Specifies that duplicate values for the managed property are removed.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: rd

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RespectPriority

> Applicable: SharePoint Server Subscription Edition

Specifies that when a mapped crawled property contains multiple values and RespectPriority is set to  true, only the first mapped crawled property is copied.
Otherwise, all mapped crawled properties that have a value are copied.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: rp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Retrievable

> Applicable: SharePoint Server Subscription Edition

Specifies whether this managed property is retrievable or not.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: r

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SafeForAnonymous

> Applicable: SharePoint Server Subscription Edition

Specifies whether it is acceptable to display the contents of the property in search results for anonymous searches.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: sfa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchApplication

> Applicable: SharePoint Server Subscription Edition

Specifies the search application that contains the managed property collection.

The type must be a valid search application name (for example, SearchApp1), or an instance of a valid SearchServiceApplication object.

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

### -SiteCollection

> Applicable: SharePoint Server Subscription Edition

Specifies that the managed properties returned are to be within the scope of a site collection (SPSite).

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

> Applicable: SharePoint Server Subscription Edition

Specifies that the managed properties returned are to be within the scope of a tenant.

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

### -Type

> Applicable: SharePoint Server Subscription Edition

Specifies the data type of the new managed property.

The type must be one of the following data types:

1 = Text

2 = Integer

3 = Decimal

4 = DateTime

5 = YesNo

6 = Binary

7 = Double

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: t

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserFlags

> Applicable: SharePoint Server Subscription Edition

Reserved for future use.

```yaml
Type: Int16
Parameter Sets: (All)
Aliases: u

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
