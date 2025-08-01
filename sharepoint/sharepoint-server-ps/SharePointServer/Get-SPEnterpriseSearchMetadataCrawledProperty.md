---
external help file: Microsoft.Office.Server.Search.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/get-spenterprisesearchmetadatacrawledproperty
applicable: SharePoint Server Subscription Edition
title: Get-SPEnterpriseSearchMetadataCrawledProperty
schema: 2.0.0
---

# Get-SPEnterpriseSearchMetadataCrawledProperty

## SYNOPSIS
Returns a crawled property.

## SYNTAX

```
Get-SPEnterpriseSearchMetadataCrawledProperty [-AssignmentCollection <SPAssignmentCollection>]
 [-Category <CategoryPipeBind>] [-Limit <String>] [-Name <String>] [-PropSet <Guid>]
 -SearchApplication <SearchServiceApplicationPipeBind> [-SiteCollection <Guid>] [-Tenant <Guid>]
 [-VariantType <Int32>] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet reads a CrawledProperty object for a crawled property that was created or updated.
You should run this cmdlet when the search functionality is configured for the first time, and after new crawled properties are discovered during a crawl.
If the Name parameter is not specified, this cmdlet returns all crawled properties for the specified category for the specified search application.
If neither the Name nor the Category parameter is specified, this cmdlet returns all crawled properties for the specified search application.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### Example 1
```powershell
$ssa = Get-SPEnterpriseSearchServiceApplication
$cat = Get-SPEnterpriseSearchMetadataCategory -SearchApplication $ssa -Identity People
Get-SPEnterpriseSearchMetadataCrawledProperty -SearchApplication $ssa -Category $cat -Limit 1
```

This example returns the first crawled property in the PeopleSearch_Scope metadata category for the default search service application.

### Example 2
```powershell
$ssa = Get-SPEnterpriseSearchServiceApplication
$cat = Get-SPEnterpriseSearchMetadataCategory -SearchApplication $ssa -Identity People
$crawledProp = Get-SPEnterpriseSearchMetadataCrawledProperty -SearchApplication $ssa -Category $cat -Name urn:schemas-microsoft-com:sharepoint:portal:profile:CellPhone
$crawledProp.GetMappedManagedProperties()
```

This example returns the mappings of a specific crawled property in the PeopleSearch_Scope metadata category for the default search service application.

## PARAMETERS

### -AssignmentCollection

> Applicable: SharePoint Server Subscription Edition

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

### -Category

> Applicable: SharePoint Server Subscription Edition

Specifies the metadata category of the crawled property to return.

The type must be a valid GUID in the form 12345678-90ab-cdef-1234-567890bcdefgh, a valid name of a metadata category, for example, MetadataCategory1, or an instance of a valid Category object.

```yaml
Type: CategoryPipeBind
Parameter Sets: (All)
Aliases: c

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Limit

> Applicable: SharePoint Server Subscription Edition

Specifies the maximum number of items to return.

Specify ALL to return all possible results.

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

### -Name

> Applicable: SharePoint Server Subscription Edition

Specifies the crawled property to retrieve.

The type must be a valid crawled property name, for example "urn:schemas-microsoft-com:sharepoint:portal:profile:UserName"

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

### -PropSet

> Applicable: SharePoint Server Subscription Edition

Specifies to return crawled properties that use the specified property set.
A property set belongs to one crawled property category.

The type must be a valid GUID that specifies the property set in the form 12345678-90ab-cdef-1234-567890bcdefgh.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: p

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchApplication

> Applicable: SharePoint Server Subscription Edition

Specifies the search application that contains the crawled property.

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

### -SiteCollection

> Applicable: SharePoint Server Subscription Edition

Specifies that the crawled properties returned are to be within the scope of a site collection (SPSite).

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

Specifies that the crawled properties returned are to be within the scope of a tenant.

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

### -VariantType

> Applicable: SharePoint Server Subscription Edition

Specifies to return crawled properties that use the specified variant type.

The type must be an integer that specifies the variant data type of the property set.


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: vt

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
