---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/add-spositescript
applicable: SharePoint Online
title: Add-SPOSiteScript
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Add-SPOSiteScript

## SYNOPSIS

Uploads a new site script for use either directly or in a site design.

## SYNTAX

```
Add-SPOSiteScript -Title <String> -Content <String> [-Description <String>] [<CommonParameters>]
```

## DESCRIPTION

Uploads a new site script for use either directly or in a site design.

## EXAMPLES

### Example 1

This example adds a new site logo from the following script in a file.

```json
{
  "$schema": "schema.json",
  "actions": [
      {
        "verb": "setSiteLogo",
        "url": "https://contoso.sharepoint.com/SiteAssets/company-logo.png"
      }
  ]
}
```

```powershell
Get-Content 'c:\scripts\site-script.json' -Raw | Add-SPOSiteScript -Title "Customer logo" -Description "Applies customer logo for customer sites"
```

### Example 2

This example sets the external sharing capabilities of the site to the ExternalUserAndGuestSharing option. We also add a site design for a Communication site (68) which uses this script.

```powershell
$script = @'
{
     "$schema": "schema.json",
         "actions": [
 {
    "verb": "setSiteExternalSharingCapability",
    "capability": "ExternalUserAndGuestSharing"
 }
         ],
         "bindata": { },
         "version": 1
 };
'@

Add-SPOSiteScript -Title "External User and Guest Sharing site script" -Description "A site script to manage the
guest access of a site" -Content $script
```

```powershell
Id          : ea9e3a52-7c12-4da8-a901-4912be8a76bc
Title       : External User and Guest Sharing site script
Description : A site script to manage theguest access of a site
Content     :
Version     : 0
```

```powershell
Add-SPOSiteDesign -Title "Communication Site with External Users and Guest Sharing" -WebTemplate "68" -SiteScripts "ea9e3a52-7c12-4da8-a901-4912be8a76bc"
```

## PARAMETERS

### -Content

> Applicable: SharePoint Online

The JSON value that describes the script. For more information, see the [JSON reference](/sharepoint/dev/declarative-customization/site-design-json-schema).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Description

> Applicable: SharePoint Online

A description of the script.

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

### -Title

> Applicable: SharePoint Online

The display name of the site design.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

### System.String

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
