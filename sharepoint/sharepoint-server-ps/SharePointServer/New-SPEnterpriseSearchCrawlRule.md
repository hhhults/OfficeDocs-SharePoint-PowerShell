---
external help file: Microsoft.Office.Server.Search.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/new-spenterprisesearchcrawlrule
applicable: SharePoint Server Subscription Edition
title: New-SPEnterpriseSearchCrawlRule
schema: 2.0.0
---

# New-SPEnterpriseSearchCrawlRule

## SYNOPSIS
Creates a new crawl rule.

## SYNTAX

```
New-SPEnterpriseSearchCrawlRule [-AccountName <String>] [-AccountPassword <SecureString>]
 [-AssignmentCollection <SPAssignmentCollection>] [-AuthenticationType <CrawlRuleAuthenticationType>]
 [-Confirm] [-ContentClass <String>] [-CrawlAsHttp <Boolean>] [-FollowComplexUrls <Boolean>]
 [-IsAdvancedRegularExpression <Boolean>] -Path <String> [-PluggableSecurityTimmerId <Int32>]
 [-Priority <Int32>] -SearchApplication <SearchServiceApplicationPipeBind> [-SuppressIndexing <Boolean>]
 -Type <CrawlRuleType> [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
The `New-SPEnterpriseSearchCrawlRule` cmdlet creates special rules for crawling items that are contained in the specified path.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
$ssa = Get-SPEnterpriseSearchServiceApplication
New-SPEnterpriseSearchCrawlRule -SearchApplication $ssa -Path https://ExampleSharePointSite -CrawlAsHttp 1 -Type InclusionRule
```

This example creates an inclusion type crawl rule for the site at https://ExampleSharePointSite.
The rule specifies that the site be crawled as an HTTP site.

## PARAMETERS

### -AccountName

> Applicable: SharePoint Server Subscription Edition

Specifies the account to use when applying the crawl rule.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AccountPassword

> Applicable: SharePoint Server Subscription Edition

Specifies the account to use when applying the crawl rule.

```yaml
Type: SecureString
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

### -AuthenticationType

> Applicable: SharePoint Server Subscription Edition

Specifies one of the following authentication types to access matching URLs:

BasicAccountRuleAccess -- Specifies the account name and password that are required for this authentication type.

CertificateRuleAccess -- Specifies the valid client certificate name that is required for this authentication type.

NTLMAccountRuleAccess -- Specifies the account name for integrated authentication.

FormRuleAccess -- Specifies a valid URL for HTTP POST or HTTP GET, public and private parameters, and a list of error pages that are used by this authentication type.

CookieRuleAccess -- Specifies private parameters and a list of error pages that are used by this authentication type.

AnonymousAccess-- Specifies that the matching URLs have to be accessed anonymously.

```yaml
Type: CrawlRuleAuthenticationType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -ContentClass

> Applicable: SharePoint Server Subscription Edition

Specifies the string that is sent to the protocol handler for any content that matches the crawl rule.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CrawlAsHttp

> Applicable: SharePoint Server Subscription Edition

Specifies whether the crawler should crawl content from a hierarchical content source as HTTP content.

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

### -FollowComplexUrls

> Applicable: SharePoint Server Subscription Edition

Specifies whether the index engine should crawl content with URLs that contain a question mark (?).

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

### -IsAdvancedRegularExpression

> Applicable: SharePoint Server Subscription Edition

Specifies whether the rule has a full regular expression syntax.

The default value is False.

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

### -Path

> Applicable: SharePoint Server Subscription Edition

Specifies a unique path to which a crawl rule applies.

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

### -PluggableSecurityTimmerId

> Applicable: SharePoint Server Subscription Edition

{{Fill PluggableSecurityTimmerId Description}}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priority

> Applicable: SharePoint Server Subscription Edition

Defines where in the list of crawl rules this crawl rule should be applied.

The priority value cannot be less than 0 or greater than or equal to the number of crawl rules for the search application.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchApplication

> Applicable: SharePoint Server Subscription Edition

Specifies the Search application that is associated with the crawl rule to be modified.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid search application name (for example, SearchApp1); or an instance of a valid SearchServiceApplication object.

```yaml
Type: SearchServiceApplicationPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SuppressIndexing

> Applicable: SharePoint Server Subscription Edition

Specifies whether the crawler should exclude the content of items that this rule applies to from the content index.

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

### -Type

> Applicable: SharePoint Server Subscription Edition

Specifies the type of crawl rule.
A value of zero (0) includes the rule, a value of 1 excludes the rule.

```yaml
Type: CrawlRuleType
Parameter Sets: (All)
Aliases: t

Required: True
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
