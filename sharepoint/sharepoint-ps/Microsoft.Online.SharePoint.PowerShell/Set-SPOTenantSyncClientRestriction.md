---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/set-spotenantsyncclientrestriction
applicable: SharePoint Online
title: Set-SPOTenantSyncClientRestriction
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Set-SPOTenantSyncClientRestriction

## SYNOPSIS

Controls tenant-wide options and restrictions specific to syncing files.

## SYNTAX

### Blocking
```
Set-SPOTenantSyncClientRestriction [-Enable] [-DomainGuids <String>] [-BlockMacSync] [<CommonParameters>]
```

### FileExclusion
```
Set-SPOTenantSyncClientRestriction [-ExcludedFileExtensions <String>] [<CommonParameters>]
```

### GrooveBlockOptions
```
Set-SPOTenantSyncClientRestriction [-GrooveBlockOption <String>] [<CommonParameters>]
```

### ReportProblemDialogFeature
```
Set-SPOTenantSyncClientRestriction -DisableReportProblemDialog <Boolean> [<CommonParameters>]
```

## DESCRIPTION

This cmdlet contains more than one parameter set. You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets. For more information about how to use parameter sets, see [Cmdlet Parameter Sets](https://msdn.microsoft.com/library/dd878348(VS.85).aspx).

You must be at least a SharePoint administrator to run the cmdlet.

Requires a valid Connect-SPOService context to identify the tenant. For information on how to connect to the tenant, see [Connect-SPOService](Connect-SPOService.md)

The **Set-SPOTenantSyncClientRestriction** cmdlet is used to control a variety of tenant-wide administrative settings related to syncing files from OneDrive and SharePoint. You may use it to:

* Set restrictions on whether users can sync items to non-domain joined machines, control the list of allowed domains, and manage whether Mac clients (which do not support domain join) can sync.

* Prevents files with specific extensions from being synced.

* Controls whether users can continue to sync OneDrive for Business libraries with the old OneDrive for Business sync client.

**Restrict non-domain joined machines from syncing**

The **Set-SPOTenantSyncClientRestriction** cmdlet can be used to enable the feature for tenancy and set the domain GUIDs in the safe recipients list. When this feature is enabled it can take up to 24 hours for the change to take effect. However, any changes to the safe domains list are reflected within five minutes.

> [!IMPORTANT]
> The new OneDrive for Business Next Generation Sync Client lets you connect and sync files from your OneDrive for Business. You can add a work or school account to the new OneDrive for Business sync client and sync all your files in OneDrive to your computer.  For more information, see [Improve your OneDrive sync experience](https://go.microsoft.com/fwlink/p/?LinkId=717436).

When the feature is enabled the following will occur:

* All OneDrive for Business Sync client requests originating from a domain that is not on the safe recipients list will be blocked.
* All Microsoft OneDrive Mac Sync client and Mac Beta client requests will not be blocked by default.
* Microsoft OneDrive mobile apps  are not blocked when this feature is enabled.
* Regardless whether a computer is managed by a device management solution, a sync relationship will not be established unless they are   joined to a domain in the Safe Recipient List.
* Any files that have been previously been synced down to your computer will not be deleted.
* When this feature is enabled, please be aware the following upload behavior:

  * New or existing files added to the client will still be uploaded to the server and will not be blocked.
  * Regardless if the computer is joined to a domain which is set in the Safe Recipient List.
  * Regardless if the computer is joined to  a domain which is not set in the Safe Recipient List.
  * And for all non-domain joined computers.

* Microsoft  OneDrive for Business sync client prior to version 15.0.4693.1000 will stop syncing existing libraries.

> [!IMPORTANT]
> In order to explicitly block Microsoft OneDrive client for Mac or OneDrive for Business Next Generation Sync Client on Mac OS X, please run the **Set-SPOTenantSyncClientRestriction** cmdlet with the **BlockMacSync** parameter set to true.  For more information about the Next Generation Sync Client for Mac OS X, see [Get started with the new OneDrive sync client on Mac OS X](https://go.microsoft.com/fwlink/?LinkID=717727).
> [!IMPORTANT]
> There is a known OneDrive for Business sync client issue where syncing is being  blocked even if a computer is joined to a domain which is  set in the Safe Recipient List. To resolve this behavior, obtain the 15.0.4719.1000 version or higher of the sync client, see [May 12, 2015, update for OneDrive for Business](https://support.microsoft.com/en-us/kb/2986244/).
> [!NOTE]
> To determine the version of your Sync client, see [What version of the sync client am I using?](https://support.office.com/en-us/article/Which-version-of-OneDrive-am-I-using-19246eae-8a51-490a-8d97-a645c151f2ba).

* The latest OneDrive for Business sync client can be downloaded from [Download OneDrive for Windows](https://go.microsoft.com/fwlink/?LinkID=404119&clcid=0x409) or [How to install OneDrive for Business for SharePoint and SharePoint Online](https://go.microsoft.com/fwlink/?LinkID=321300&amp;clcid=0x409).

> [!IMPORTANT]
> This capability doesn't support Microsoft Entra joined or Workplace joined devices.

For additional information about how to troubleshoot the OneDrive for Business sync client, see [How to switch from an MSI installation of OneDrive for Business (formerly SkyDrive Pro) standalone to a Click-To-Run installation of OneDrive for Business (formerly SkyDrive Pro) standalone](https://go.microsoft.com/fwlink/?LinkId=526386&clcid=0x409).

**Block specific file extensions from syncing**

The **Set-SPOTenantSyncClientRestriction** cmdlet can be used to configure a list of file extensions that should not be synced by the OneDrive sync client, such as .PST files.

Any file extension may be blocked using this feature, but note that it may take up to 24 hours for a change to take affect across all user devices. When this feature is enabled, users syncing any file that is in the exclusion list will see an error message informing them of the block.

> [!IMPORTANT]
> This feature is only supported by the new OneDrive for Business sync client. To determine the version of your Sync client, see [What version of the sync client am I using?](https://support.office.com/en-us/article/Which-version-of-OneDrive-am-I-using-19246eae-8a51-490a-8d97-a645c151f2ba).

## EXAMPLES

### EXAMPLE 1

```powershell
Set-SPOTenantSyncClientRestriction  -Enable -DomainGuids "786548DD-877B-4760-A749-6B1EFBC1190A; 877564FF-877B-4760-A749-6B1EFBC1190A"
```

This example enables the feature for the  tenancy and adds the domains GUIDs to the safe recipient list.

### EXAMPLE 2

```powershell
Set-SPOTenantSyncClientRestriction  -Enable -DomainGuids "786548DD-877B-4760-A749-6B1EFBC1190A; 877564FF-877B-4760-A749-6B1EFBC1190A" -BlockMacSync:$true
```

This example turns on the Block Mac sync functionality.

### EXAMPLE 3

```powershell
Set-SPOTenantSyncClientRestriction  -ExcludedFileExtensions "pptx;docx;xlsx"
```

This example blocks syncing of PowerPoint, Word, and Excel file types using the new sync client (OneDrive.exe).

### EXAMPLE 4

```powershell
Set-SPOTenantSyncClientRestriction  -ExcludedFileExtensions ""
```

This example clears the ExcludedFileExtension list and lets all file types synced with the new client (OneDrive.exe).

## PARAMETERS

### -BlockMacSync

> Applicable: SharePoint Online

Block Mac sync clients-- the Beta version and the new sync client (OneDrive.exe).
The values for this parameter are True and False. The default value is False.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Blocking
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableReportProblemDialog

> Applicable: SharePoint Online

```yaml
Type: System.Boolean
Parameter Sets: ReportProblemDialogFeature
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainGuids

> Applicable: SharePoint Online

Sets the [domain GUID](/powershell/module/activedirectory/get-addomain) of the computer domain membership to add to the safe recipient list. Requires a minimum of one domain GUID. The maximum number of domain GUIDs allowed is 125.

```yaml
Type: System.String
Parameter Sets: Blocking
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enable

> Applicable: SharePoint Online

Enables the feature to block sync originating from domains that are not present in the safe recipients list.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Blocking
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludedFileExtensions

> Applicable: SharePoint Online

Blocks certain file types from syncing with the new sync client (OneDrive.exe).

> [!NOTE]
> It may take up to one hour for changes to take effect.

```yaml
Type: System.String
Parameter Sets: FileExclusion
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GrooveBlockOption
{{ Fill GrooveBlockOption Description }}

```yaml
Type: System.String
Parameter Sets: GrooveBlockOptions
Aliases:
Accepted values: OptOut, HardOptIn, SoftOptIn

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
