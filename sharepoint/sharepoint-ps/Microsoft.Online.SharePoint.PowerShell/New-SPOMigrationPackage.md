---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/new-spomigrationpackage
applicable: SharePoint Online
title: New-SPOMigrationPackage
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# New-SPOMigrationPackage

## SYNOPSIS
Cmdlet to create a new migration package based on source files in a local or network shared folder.

> [!NOTE]
> This cmdlet has been deprecated. To migrate to SharePoint and Microsoft 365 using PowerShell, see
> [Migrate to SharePoint using PowerShell](/sharepointmigration/overview-spmt-ps-cmdlets).

## SYNTAX

```
New-SPOMigrationPackage [-SourceFilesPath] <String> [-OutputPackagePath] <String> [[-TargetWebUrl] <String>]
 [[-TargetDocumentLibraryPath] <String>] [[-TargetDocumentLibrarySubFolderPath] <String>]
 [-IncludeFileSharePermissions] [-ReplaceInvalidCharacters] [-IgnoreHidden] [-NoLogFile] [-NoAzureADLookup]
 [<CommonParameters>]
```

## DESCRIPTION

Cmdlet to create a new migration package based on source files in a local or network shared folder.

## EXAMPLES

### EXAMPLE 1

```powershell
New-SPOMigrationPackage -SourceFilesPath \\fileserver\share\folder1 -OutputPackagePath d:\MigrationPackages\Folder1_SrcPkg

New-SPOMigrationPackage -SourceFilesPath \\fileserver\share\folder1 -OutputPackagePath d:\MigrationPackages\Folder1_SrcPkg -TargetWebUrl https://contoso.sharepoint.com/sites/TargetSite/TargetWeb -TargetDocumentLibraryPath "Shared Documents" -TargetDocumentLibrarySubFolderPath "Sub Folder/Target Folder"
```

This example creates a new set of migration source package metadata files, using default URL values, in the d:\MigrationPackages\Folder1_SrcPkg directory based on content files found in the \\fileserver\share\folder1 source location.

### EXAMPLE 2

```powershell
New-SPOMigrationPackage -SourceFilesPath \\fileserver\share\folder1 -OutputPackagePath d:\MigrationPackages\Folder1_SrcPkg -TargetWebUrl https://contoso.sharepoint.com/sites/TargetSite/TargetWeb -TargetDocumentLibraryPath "Shared Documents"
```

This example creates a new set of migration source package metadata files in the d:\MigrationPackages\Folder1_SrcPkg directory based on content files found in the \\fileserver\share\folder1 source location. The package is prepared using the document library path "https://contoso.sharepoint.com/sites/TargetSite/TargetWeb/Shared Documents".

## PARAMETERS

### -IgnoreHidden

> Applicable: SharePoint Online

Switch to ignore hidden files and folders.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeFileSharePermissions

> Applicable: SharePoint Online

Used to include permissions and sharing information into the generated manifest files in the package metadata.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoAzureADLookup

> Applicable: SharePoint Online

Switch to not lookup local user accounts in Microsoft Entra ID.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoLogFile

> Applicable: SharePoint Online

Used to not create a log file. The default is to create a new CreateMigrationPackage log file within the directory specified within the OutputPackagePath parameter.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputPackagePath

> Applicable: SharePoint Online

The directory location where the output package metadata files will be saved. If the directory does not exist, it will be created.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplaceInvalidCharacters

> Applicable: SharePoint Online

Switch to replace characters in file and folder names that would be invalid in SharePoint Online.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceFilesPath

> Applicable: SharePoint Online

The directory location where the source content files exist. This directory will be enumerated to create the package metadata files.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDocumentLibraryPath

> Applicable: SharePoint Online

The web relative document library to use as the document library part of the base URL in the package metadata. If this is not supplied, "Documents" will be used within the package metadata instead.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDocumentLibrarySubFolderPath

> Applicable: SharePoint Online

Specifies the document library relative subfolder to use as the folder path part of the base URL in the package metadata. If this is not provided, no value will be used within the package metadata. The files will be homed under the document library root.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetWebUrl

> Applicable: SharePoint Online

The fully qualified web URL to use as the web address part of the base URL in the package metadata. If this is not provided, "`https://fileserver/sites/user`" will be used instead within the package metadata.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

Limits on the SPO package size and file size

|    Limit     | Max Size (Gb) |                                   Description                                    |
| ------------ | :-----------: | -------------------------------------------------------------------------------- |
| Package Size |      2-4      | The whole package can't exceed 4Gb                                               |
| File Size    |       2       | A single file inside the source folder can't exceed 2 Gb.                        |
| Target Size  |       -       | target site should remain non-accessible to end user until migration is complete |

Limits on HTTP Get

|       Limit       | API Get (chars) |                      Description                       |
| ----------------- | :-------------: | ------------------------------------------------------ |
| Action GET on API |    260 chars    | The size of the API GET request can't exceed 260 chars |

## RELATED LINKS
