---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/submit-spomigrationjob
applicable: SharePoint Online
title: Submit-SPOMigrationJob
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Submit-SPOMigrationJob

## SYNOPSIS

**Note**: This cmdlet has been deprecated. To migrate to SharePoint and Microsoft 365 using PowerShell, see [Migrate to SharePoint using PowerShell](/sharepointmigration/overview-spmt-ps-cmdlets).

Cmdlet to submit a new migration job referenced to a previously uploaded package in Azure Blob storage into to a site collection.

## SYNTAX

### AzureLocationsInline
```
Submit-SPOMigrationJob [-TargetWebUrl] <String> [-FileContainerUri] <String> [-PackageContainerUri] <String>
 [-AzureQueueUri <String>] -Credentials <CredentialCmdletPipeBind> [-NoLogFile]
 [-EncryptionParameters <EncryptionParameters>] [<CommonParameters>]
```

### AzureLocationsPipebind
```
Submit-SPOMigrationJob [-TargetWebUrl] <String>
 [-MigrationPackageAzureLocations] <MigrationPackageAzureLocations> -Credentials <CredentialCmdletPipeBind>
 [-NoLogFile] [-EncryptionParameters <EncryptionParameters>] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see Cmdlet Parameter Sets.

This cmdlet returns a GUID value which represents the MigrationJobId, or returns an empty GUID if the job was not successfully created.

## EXAMPLES

### EXAMPLE 1

```powershell
Submit-SPOMigrationJob -TargetUrl https://contoso.sharepoint.com/sites/TargetSite/TargetWeb -FileContainerUri "https://migrationstore.blob.core.windows.net/migration-files?sv=2014-02-14&sr=c&sig=THTTJoeGHysxRLgv22j473XYS2blH1YAVIdsfWrPhq8=&se=2015-04-06T05:09:36Z&sp=rl" -PackageContainerUri "https://migrationstore.blob.core.windows.net/migration-package?sv=2014-02-14&sr=c&sig=2PCBJtiXsVWiK5GrY7jBEdyEAwtunQNJLH8uo6I0+Ew=&se=2015-04-06T05:09:37Z&sp=rwl"
```

This example creates a new migration job in the target site collection for the web at the URL '<https://contoso.sharepoint.com/sites/TargetSite/TargetWeb'.> The migration job includes information about the file and package metadata Azure Storage containers that are passed into the command.

### EXAMPLE 2

```powershell
Submit-SPOMigrationJob -TargetUrl https://contoso.sharepoint.com/sites/TargetSite/TargetWeb -MigrationPackageAzureLocations $azurelocations
```

This example creates a new migration job in the target site collection for the web at the URL '<https://contoso.sharepoint.com/sites/TargetSite/TargetWeb'.> The migration job includes information about the file and package metadata Azure Storage containers that are passed into the command.

## PARAMETERS

### -AzureQueueUri

> Applicable: SharePoint Online

An optional fully qualified URL and SAS token representing the Azure Storage Reporting Queue where import operations will list events during import.

```yaml
Type: System.String
Parameter Sets: AzureLocationsInline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credentials

> Applicable: SharePoint Online

Optional credentials of a site collection administrator to use to connect to the site collection. The credentials should supply the username in UPN format (e.g. user@company.onmicrosoft.com). If this property is not set, the current tenant admin credentials from the session's previous call to `Connect-SPOService` will be used to connect to the site collection.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.CredentialCmdletPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionParameters

> Applicable: SharePoint Online

An EncryptionParameters object. See [New-SPOMigrationEncryptionParameters](/powershell/module/sharepoint-online/new-spomigrationencryptionparameters) for more information.

```yaml
Type: Microsoft.Online.SharePoint.Migration.EncryptionParameters
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileContainerUri

> Applicable: SharePoint Online

A fully qualified URL and SAS token representing the Azure Blob Storage container that holds the package content files.

```yaml
Type: System.String
Parameter Sets: AzureLocationsInline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MigrationPackageAzureLocations

> Applicable: SharePoint Online

A set of fully qualified URLs and SAS tokens representing the Azure Blob Storage containers that hold the package content and metadata files and an optional Azure Storage Reporting Queue. This object is returned during successful processing of the `Set-SPOMigrationPackageAzureSource` cmdlet.

```yaml
Type: Microsoft.Online.SharePoint.Migration.MigrationPackageAzureLocations
Parameter Sets: AzureLocationsPipebind
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NoLogFile

> Applicable: SharePoint Online

Indicates to not create a log file. The default is to create a new CreateMigrationJob log file within the current directory.

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

### -PackageContainerUri

> Applicable: SharePoint Online

A fully qualified URL and SAS token representing the Azure Blob Storage container that holds the package metadata files.

```yaml
Type: System.String
Parameter Sets: AzureLocationsInline
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetWebUrl

> Applicable: SharePoint Online

The fully qualified target web URL where the package will be imported into. This must include the same TargetWebURL that was used during `ConvertTo-SPOMigrationTargetedPackage`.

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

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.Online.SharePoint.Migration.MigrationPackageAzureLocations

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
