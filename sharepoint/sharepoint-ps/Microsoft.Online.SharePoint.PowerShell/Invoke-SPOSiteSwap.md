---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/invoke-spositeswap
applicable: SharePoint Online
title: Invoke-SPOSiteSwap
schema: 2.0.0
ms.author: divyasru
ms.reviewer:
---

# Invoke-SPOSiteSwap

## SYNOPSIS

Invokes a job to swap the location of a site with another site while archiving the original site.

## SYNTAX

```
Invoke-SPOSiteSwap [-SourceUrl] <String> [[-TargetUrl] <String>] [-ArchiveUrl] <String> [-DisableRedirection]
 [-Force] [-NoWait] [<CommonParameters>]
```

## DESCRIPTION

Swaps the location of a source site with a target site while archiving the original target site.

Please note, the target site must be either:

- The root site, for example `https://tenant-name.sharepoint.com`; or
- The search center site, for example `https://tenant-name.sharepoint.com/search`.

When the swap is initiated, the target site is moved to the archive location and the source site is moved to the target location. By default, a site redirect is created at the source location that will redirect traffic to the target location.

If the target is the root site at `https://tenant-name.sharepoint.com`, then the following preparation activities should be performed prior to performing the swap:

1. Any Featured links defined in SharePoint Start Page at `https://tenant-name.sharepoint.com/_layouts/15/sharepoint.aspx` will not be displayed after performing the swap. If required, the Featured links should be documented so they can be manually recreated after the swap.
2. Functionality such as external sharing and application interfaces are dependent on the policies and permissions defined at the root site. Review the source site to ensure that it has the required policies and permissions as per the existing root site. This includes external sharing settings as well as site permissions.
3. Larger tenants that have more than ~10,000 licenses will need to run the [Page Diagnostic Tool](/office365/enterprise/page-diagnostics-for-spo) against the source site (ensure that the user running the Page Diagnostic Tool has edit rights on the source site). Any analysis results that have the category Attention required (Red) or Improvement opportunities (Orange) will need to be remediated before performing the swap.

The source and target sites can't be connected to an Office 365 group. They also can't be hub sites or associated with a hub.
If a site is a hub site, unregister it as a hub site, swap the root site, and then register the site as a hub site. If a site is associated with a hub, disassociate the site, swap the root site, and then reassociate the site.

If the Publishing feature has previously been activated or is currently activated on the source site, Invoke-SPOSiteSwap cannot be used.

## EXAMPLES

### EXAMPLE 1

```powershell
Invoke-SPOSiteSwap -SourceUrl https://contoso.sharepoint.com/sites/CommunicationSite -TargetUrl https://contoso.sharepoint.com -ArchiveUrl https://contoso.sharepoint.com/sites/Archive
```

Archives the existing site at <https://contoso.sharepoint.com> to <https://contoso.sharepoint.com/sites/Archive> and moves <https://contoso.sharepoint.com/sites/CommunicationSite> to <https://contoso.sharepoint.com.> A site redirect will be created at <https://contoso.sharepoint.com/sites/CommunicationSite> that will redirect any requests to <https://contoso.sharepoint.com.>

### EXAMPLE 2

```powershell
Invoke-SPOSiteSwap -SourceUrl https://contoso.sharepoint.com/sites/SearchSite -TargetUrl https://contoso.sharepoint.com/search -ArchiveUrl https://contoso.sharepoint.com/sites/Archive
```

Archives the existing Search Center site at <https://contoso.sharepoint.com/search> to <https://contoso.sharepoint.com/sites/Archive> and moves the <https://contoso.sharepoint.com/sites/SearchSite> to <https://contoso.sharepoint.com/search.> A site redirect be created at <https://contoso.sharepoint.com/sites/SearchSite> that will redirect any requests to <https://contoso.sharepoint.com/search.>

### EXAMPLE 3

```powershell
Invoke-SPOSiteSwap -SourceUrl https://contoso.sharepoint.com/sites/CommunicationSite -TargetUrl https://contoso.sharepoint.com -ArchiveUrl https://contoso.sharepoint.com/sites/Archive -DisableRedirection
```

Archives the existing site at <https://contoso.sharepoint.com> to <https://contoso.sharepoint.com/sites/Archive> and moves <https://contoso.sharepoint.com/sites/CommunicationSite> to <https://contoso.sharepoint.com.> A site redirect will not be created at <https://contoso.sharepoint.com/sites/CommunicationSite.>

### EXAMPLE 4

```powershell
Invoke-SPOSiteSwap -SourceUrl https://contoso.sharepoint.com/sites/SearchSite -TargetUrl https://contoso.sharepoint.com/search -ArchiveUrl https://contoso.sharepoint.com/sites/Archive -Force
```

Archives the existing Search Center site at <https://contoso.sharepoint.com/search> to <https://contoso.sharepoint.com/sites/Archive> and moves the <https://contoso.sharepoint.com/sites/SearchSite> to <https://contoso.sharepoint.com/search.> A site redirect be created at <https://contoso.sharepoint.com/sites/SearchSite> that will redirect any requests to <https://contoso.sharepoint.com/search.> Any warnings identified by the Page Diagnostic Tool will be ignored and the swap will be initiated. However, any errors identified by the Page Diagnostic Tool will still prevent the swap from being initiated.

## PARAMETERS

### -ArchiveUrl

> Applicable: SharePoint Online

URL that the target site will be archived to. There should be no existing site, including a deleted site in the Recycle Bin, at this location before performing the swap.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableRedirection

> Applicable: SharePoint Online

Disables the site redirect from being created at the Source URL location.

```yaml
Type: Switch Parameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force

> Applicable: SharePoint Online

Overrides and ignores any warnings that have been identified by the Page Diagnostic Tool that are preventing a swap from being initiated.

For example, if you receive the warning "Invoke-SPOSiteSwap : Errors: 0; Warnings: 1; Details: 2 items are not in CDN, please enable CDN." Warnings can be overriden using this parameter but the items should be reviewed and resolved for long-term stability and performance.

Any errors identified by the Page Diagnostic Tool will still always prevent a swap from being initiated regardless of this parameter.

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

### -NoWait

> Applicable: SharePoint Online

This parameter is reserved for internal Microsoft use.

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

### -SourceUrl

> Applicable: SharePoint Online

URL of the source site. The site at this location must exist before performing the swap.

If the target is the root site at `https://tenant-name.sharepoint.com` then the source site must be either a Modern Team Site (STS#3) or a Communication Site (SITEPAGEPUBLISHING#0) and **the publishing feature can never have been activated on the source site**.

If the target is the search center site at `https://tenant-name.sharepoint.com/search` then the source site must be either a Search Center Site (SRCHCEN#0) or a Basic Search Center Site (SRCHCENTERLITE#0).

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetUrl

> Applicable: SharePoint Online

URL of the target site that the source site will be swapped to. The site at this location must exist before performing the swap.

The target site must be either:

- The root site at `https://tenant-name.sharepoint.com` or
- The search center site at `https://tenant-name.sharepoint.com/search`

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
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

[Getting started with SharePoint Online Management Shell](/powershell/sharepoint/sharepoint-online/connect-sharepoint-online)
[Modernize your root site](/sharepoint/modern-root-site)
[Manage site redirects](/sharepoint/manage-site-redirects)
[Page Diagnostic Tool](/office365/enterprise/page-diagnostics-for-spo)
