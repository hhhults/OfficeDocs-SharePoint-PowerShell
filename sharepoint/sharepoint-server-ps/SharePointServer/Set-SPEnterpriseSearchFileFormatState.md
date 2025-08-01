---
external help file: Microsoft.Office.Server.Search.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-spenterprisesearchfileformatstate
applicable: SharePoint Server Subscription Edition
title: Set-SPEnterpriseSearchFileFormatState
schema: 2.0.0
---

# Set-SPEnterpriseSearchFileFormatState

## SYNOPSIS
Sets the activation state of a parser for a given file format.

## SYNTAX

```
Set-SPEnterpriseSearchFileFormatState [-Identity] <DocumentParserFileFormatStatePipeBind> [-Enable] <Boolean>
 -SearchApplication <SearchServiceApplicationPipeBind> [-AssignmentCollection <SPAssignmentCollection>]
 [-Confirm] [-WhatIf] [-UseIFilter <Boolean>] [<CommonParameters>]
```

## DESCRIPTION
The `Set-SPEnterpriseSearchFileFormatState` cmdlet sets the activation state of the parser that corresponds to the specified file format.
By default, the initial activation state of all file formats is $TRUE (enabled).
Use this cmdlet to temporarily disable a malfunctioning parser.
The system will only consider the change after a restart of the content processing components.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
$ssa = Get-SPEnterpriseSearchServiceApplication
Set-SPEnterpriseSearchFileFormatState -SearchApplication $ssa -Identity PDF -Enable $false
```

This example uses the `Set-SPEnterpriseSearchFileFormatState` cmdlet to disable the parser for the file format "PDF".

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the identification of the format to be disabled or enabled.

```yaml
Type: DocumentParserFileFormatStatePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Enable

> Applicable: SharePoint Server Subscription Edition

Specifies the activation state of the parser that corresponds to the specified file format.
The activation state can be $FALSE (disabled) or $TRUE (enabled).

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchApplication

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the search application.
The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid SearchServiceApplication object.

```yaml
Type: SearchServiceApplicationPipeBind
Parameter Sets: (All)
Aliases:

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

### -UseIFilter

> Applicable: SharePoint Server Subscription Edition

Specifies use of a third-party iFilter when parsing the file format. UseIFilter can be $false (built-in format handler is used) or $TRUE (third-party iFilter is used). $false is the default value.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216 (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-SPEnterpriseSearchFileFormat](New-SPEnterpriseSearchFileFormat.md)

[Get-SPEnterpriseSearchFileFormat](Get-SPEnterpriseSearchFileFormat.md)

[Remove-SPEnterpriseSearchFileFormat](Remove-SPEnterpriseSearchFileFormat.md)
