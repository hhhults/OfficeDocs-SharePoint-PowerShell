---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/add-spotenantcdnorigin
applicable: SharePoint Online
title: Add-SPOTenantCdnOrigin
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Add-SPOTenantCdnOrigin

## SYNOPSIS

Configures a new origin to public or private content delivery network (CDN). Requires Tenant administrator permissions.

## SYNTAX

```
Add-SPOTenantCdnOrigin -OriginUrl <String> -CdnType <SPOTenantCdnType> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Configures a new origin to public or private CDN, on either Tenant level or on a single Site level. Effectively, a tenant admin points out to a document library, or a folder in the document library and requests that content in that library should be retrievable by using a CDN.

You must have the SharePoint Admin role and be a site collection administrator to run the cmdlet.

## EXAMPLES

### Example 1

```
Add-SPOTenantCdnOrigin -CdnType public -OriginUrl /sites/site/subfolder
```

This example configures a public CDN on a site level.

## PARAMETERS

### -CdnType

> Applicable: SharePoint Online

Specifies the CDN type. The valid values are:  public or private.

```yaml
Type: Microsoft.Online.SharePoint.TenantAdministration.SPOTenantCdnType
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OriginUrl

> Applicable: SharePoint Online

Specifies a path to the doc library to be configured. It can be provided in two ways: relative path, or a mask.

Relative-Relative path depends on the OriginScope.  If the originScope is Tenant, a path must be a relative path under the tenant root. If the originScope is Site, a path must be a relative path under the given Site.  The path must point to the valid Document Library or a folder within a document library.

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

### -Confirm

> Applicable: SharePoint Online

Prompts you for confirmation before running the cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

> Applicable: SharePoint Online

Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](<https://go.microsoft.com/fwlink/?LinkID=113216).>

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
