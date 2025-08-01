---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spomigrationjobprogress
applicable: SharePoint Online
title: Get-SPOMigrationJobProgress
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Get-SPOMigrationJobProgress

## SYNOPSIS

**Note**: This cmdlet has been deprecated. To migrate to SharePoint and Microsoft 365 using PowerShell, see [Migrate to SharePoint using PowerShell](/sharepointmigration/overview-spmt-ps-cmdlets).

This cmdlet lets you report on SPO migration jobs that are in progress.

## SYNTAX

### AzureLocationsInline
```
Get-SPOMigrationJobProgress [-TargetWebUrl <String>] -AzureQueueUri <String>
 -Credentials <CredentialCmdletPipeBind> [-JobIds <Guid[]>] [-EncryptionParameters <EncryptionParameters>]
 [-DontWaitForEndJob] [-NoLogFile] [<CommonParameters>]
```

### AzureLocationsImplicit
```
Get-SPOMigrationJobProgress [-TargetWebUrl <String>] -Credentials <CredentialCmdletPipeBind>
 -MigrationPackageAzureLocations <MigrationPackageAzureLocations> [-JobIds <Guid[]>]
 [-EncryptionParameters <EncryptionParameters>] [-DontWaitForEndJob] [-NoLogFile] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet lets you report on SPO migration jobs that are in progress.

## EXAMPLES

### EXAMPLE 1

```powershell
$myQueueUri = <uri to azure report queue>

Get-SPOMigrationJobProgress -AzureQueueUri $myQueueUri
```

This will report on ALL jobs within the report queue.

### EXAMPLE 2

```powershell
$jobIds = @(<jobid1>,<jobId2>....)

Get-SPOMigrationJobProgress  -AzureQueueUri $myQueueUri -JobIds $jobIds
```

This will report only jobs defined within the $jobIds collection from the report queue.

### EXAMPLE 3

```powershell
$targetWebUrl = <myTargetWebUrl>
$creds = <my site credentials>

Get-SPOMigrationJobProgress - AzureQueueUri $myQueueUri - TargetWebUrl $targetWebUrl  -Credentials $creds
```

This will report on any currently queued or in progress jobs and wait for all jobs to complete.

### EXAMPLE 4

```powershell
$targetWebUrl = <myTargetWebUrl>
$creds = <my site credentials>

Get-SPOMigrationJobProgress - AzureQueueUri $myQueueUri - TargetWebUrl  $targetWebUrl -Credentials $creds  -DontWaitForJobEnd
```

This will report on any currently queued or in progress jobs and not wait for all jobs to complete.

## PARAMETERS

### -AzureQueueUri

> Applicable: SharePoint Online

An optional fully qualified URL and SAS token representing the Azure Storage Reporting Queue where import operations will list events during import.

```yaml
Type: System.String
Parameter Sets: AzureLocationsInline
Aliases:

Required: True
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

### -DontWaitForEndJob

> Applicable: SharePoint Online

Tells the cmdlet to not wait for the job to end. It will only process as many messages as are currently in the queue and then terminate. If this flag is set to $false, it will wait for the job to end before terminating.

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

### -EncryptionParameters

> Applicable: SharePoint Online

An EncryptionParameters object. See New-SPOMigrationEncryptionParameters https://learn.microsoft.com/powershell/module/sharepoint-online/new-spomigrationencryptionparameters for more information.

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

### -JobIds

> Applicable: SharePoint Online

Id of a previously created migration job that exists on the target site collection.

```yaml
Type: System.Guid[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MigrationPackageAzureLocations

> Applicable: SharePoint Online

A set of fully qualified URLs and SAS tokens representing the Azure Blob Storage containers that hold the package content and metadata files and an optional Azure Storage Reporting Queue. This object is returned during successful processing of the `Set-SPOMigrationPackageAzureSource`

```yaml
Type: Microsoft.Online.SharePoint.Migration.MigrationPackageAzureLocations
Parameter Sets: AzureLocationsImplicit
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoLogFile

> Applicable: SharePoint Online

Indicates to not create a log file. The default is to create a new CopyMigrationPackage log file within the directory specified within the SourcePackagePath parameter.

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

### -TargetWebUrl

> Applicable: SharePoint Online

The fully qualified target web URL where the package will be imported into. This must include the same TargetWebURL that was used during `ConvertTo-SPOMigrationTargetedPackage`.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

## RELATED LINKS
