---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/import-spweb
applicable: SharePoint Server Subscription Edition
title: Import-SPWeb
schema: 2.0.0
---

# Import-SPWeb

## SYNOPSIS

Imports a web, list, or library.


## SYNTAX

```
Import-SPWeb [-Identity] <SPWebPipeBind> -Path <String> [-ActivateSolutions]
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-Force] [-HaltOnError] [-HaltOnWarning]
 [-IncludeUserCustomAction <SPIncludeUserCustomAction>] [-IncludeUserSecurity] [-NoFileCompression]
 [-NoLogFile] [-UpdateVersions <SPUpdateVersions>] [-WhatIf] [-PreserveDeletedUserMetadataReferences]
 [<CommonParameters>]
```

## DESCRIPTION
The Import-SPWeb cmdlet imports a web, list, or library.
The capability to import from a library is a new feature in SharePoint Products.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
Import-SPWeb https://site -Path export.cmp -UpdateVersions Overwrite
```

This example imports the contents of export.cmp into a site at https://site, overwriting the versioned content on the site with the contents of the export.cmp file.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the URL or GUID of the Web to import into.

The type must be a valid URL, GUID, or object; for example, a valid URL, in the form https://server_name, or a GUID, in the form, 1234-4567-5678a.

```yaml
Type: SPWebPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Path

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the import file.

If the NoFileCompression parameter is used, a directory must be specified; otherwise, any file format is valid.

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

### -ActivateSolutions

> Applicable: SharePoint Server Subscription Edition

Specifies whether user solutions are activated during import.

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

### -Force

> Applicable: SharePoint Server Subscription Edition

This parameter has no function in this cmdlet.

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

### -HaltOnError

> Applicable: SharePoint Server Subscription Edition

Stops the import process when an error occurs.

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

### -HaltOnWarning

> Applicable: SharePoint Server Subscription Edition

Stops the import process when a warning occurs.

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

### -IncludeUserCustomAction

> Applicable: SharePoint Server Subscription Edition

Specifies whether User Custom Actions are included during import.

Valid values are:

All, None

```yaml
Type: SPIncludeUserCustomAction
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeUserSecurity

> Applicable: SharePoint Server Subscription Edition

Preserves the user security settings.

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

### -NoFileCompression

> Applicable: SharePoint Server Subscription Edition

Either enables or disables file compression in the import package.
The import package is stored in the folder specified by the Path parameter or Identity parameter.
We recommend that you use this parameter for performance reasons.
If compression is enabled, the import process can increase by approximately 30 percent.

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

### -NoLogFile

> Applicable: SharePoint Server Subscription Edition

Suppresses the generation of an import log file.
If this parameter is absent, the Import-SPWeb cmdlet will generate an export log file in the same location as the export package.
The log file uses Unified Logging Service (ULS).

We recommend that you use this parameter.
However, for performance reasons, you might not want to generate a log file.

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

### -UpdateVersions

> Applicable: SharePoint Server Subscription Edition

Indicates how to resolve situations where a file to be imported to a site already exists in that site.
If the UpdateVersions parameter is absent, the import operation by default uses a value of 1 (Append).

The type must be any one of the following:

-Append, which adds new versions to the current file

-Overwrite the file and all of its versions (delete then insert)

-Ignore the file if it exists on the destination

The default value is Add new versions to the current file.

Valid values are:

Append, Ignore, Overwrite

```yaml
Type: SPUpdateVersions
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

### -PreserveDeletedUserMetadataReferences

> Applicable: SharePoint Server Subscription Edition

Attempts to opulates the 'Author' ('Created By') field for items even if the SPUser object was marked as deleted on the destination site.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
