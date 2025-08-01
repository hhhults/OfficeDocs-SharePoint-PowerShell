---
external help file: Microsoft.Office.InfoPath.Server.dll-help.xml
Module Name: Microsoft.SharePoint.Powershell
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/export-spinfopathadministrationfiles
applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019
title: Export-SPInfoPathAdministrationFiles
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# Export-SPInfoPathAdministrationFiles

## SYNOPSIS
Saves InfoPath form templates on the SharePoint Central Administration Web site and .udcx files to a .cab file.

## SYNTAX

```
Export-SPInfoPathAdministrationFiles [-Path] <String> [-AssignmentCollection <SPAssignmentCollection>]
 [-Confirm] [-Identity <SPFormsServicePipeBind>] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
The Export-SPInfoPathAdministrationFiles cmdlet saves all InfoPath form templates (.xsn files) and universal data connections (.udcx files) that are located on the Central Administration page.
The backup package includes all workflow forms in InfoPath that were deployed by an administrator and not included with SharePoint Server, and includes browser forms that were deployed by an administrator.
The backup package is output to the specified .cab file.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```
Export-SPInfoPathAdministrationFiles -path d:\file.cab
```

This example saves all InfoPath form templates (.xsn files) and universal data connections (.udcx files) located on the SharePoint Central Administration Web site in a compressed cabinet file named file.cab.

## PARAMETERS

### -Path

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the location and name of the output .cab file.

The type must be a valid file path, in the form \\\\ipadmin\folder\backups1\ipfsfiles.cab.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -AssignmentCollection

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

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

### -Identity

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the site collection that contains the InfoPath form template and Central Administration .udcx files to export.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid URL, in the form https://server_name; or an instance of a valid SPSite object.

```yaml
Type: SPFormsServicePipeBind
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
