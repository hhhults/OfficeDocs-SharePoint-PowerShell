---
external help file: Microsoft.Office.Server.Search.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/get-spenterprisesearchfileformat
applicable: SharePoint Server Subscription Edition
title: Get-SPEnterpriseSearchFileFormat
schema: 2.0.0
---

# Get-SPEnterpriseSearchFileFormat

## SYNOPSIS

Retrieves all parseable file formats.


## SYNTAX

```
Get-SPEnterpriseSearchFileFormat [[-Identity] <DocumentParserFileFormatPipeBind>]
 -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
 [<CommonParameters>]
```

## DESCRIPTION

The Get-SPEnterpriseSearchFileFormat cmdlet returns the file format information for a given format ID.
If no format ID is provided, the cmdlet returns all the parseable file formats.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).


## EXAMPLES

### EXAMPLE 1
```powershell
$ssa = Get-SPEnterpriseSearchServiceApplication
Get-SPEnterpriseSearchFileFormat -SearchApplication $ssa
```

This example uses the Get-SPEnterpriseSearchFileFormat to retrieve all parseable file formats in the search service application referenced by $ssa.

### EXAMPLE 2
```powershell
$ssa = Get-SPEnterpriseSearchServiceApplication
Get-SPEnterpriseSearchFileFormat -SearchApplication $ssa -Identity DOCX
```

This example uses the Get-SPEnterpriseSearchFileFormat cmdlet to retrieve information about the file format DOCX in the search service application referenced by `$ssa`.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the format ID for which to retrieve file format information.

```yaml
Type: DocumentParserFileFormatPipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchApplication

> Applicable: SharePoint Server Subscription Edition

Specifies the search application for which to retrieve file format information.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid SearchServiceApplication object.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-SPEnterpriseSearchFileFormat](New-SPEnterpriseSearchFileFormat.md)

[Set-SPEnterpriseSearchFileFormatState](Set-SPEnterpriseSearchFileFormatState.md)

[Remove-SPEnterpriseSearchFileFormat](Remove-SPEnterpriseSearchFileFormat.md)
