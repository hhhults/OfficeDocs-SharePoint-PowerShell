---
external help file: Microsoft.Office.Server.UserProfiles.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/update-sprepopulatemicroblogfeedcache
applicable: SharePoint Server Subscription Edition
title: Update-SPRepopulateMicroblogFeedCache
schema: 2.0.0
---

# Update-SPRepopulateMicroblogFeedCache

## SYNOPSIS

Refreshes the microblog feed cache.

## SYNTAX

### (Default)

```
Update-SPRepopulateMicroblogFeedCache [-AccountName <String>]
 -ProfileServiceApplicationProxy <SPServiceApplicationProxyPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-SiteSubscription <SPSiteSubscriptionPipeBind>]
 [-SiteUrl <String>] [<CommonParameters>]
```

### Default

```
Update-SPRepopulateMicroblogFeedCache [-AccountName <String>]
 -ProfileServiceApplicationProxy <SPServiceApplicationProxyPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-SiteSubscription <SPSiteSubscriptionPipeBind>]
 [-SiteUrl <String>] [<CommonParameters>]
```

### FollowableList

```
Update-SPRepopulateMicroblogFeedCache -ProfileServiceApplicationProxy <SPServiceApplicationProxyPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] -SiteSubscription <SPSiteSubscriptionPipeBind> -ListId <Guid>
 -ListRootFolderUrl <String> -SiteId <Guid> -WebId <Guid> [<CommonParameters>]
```

## DESCRIPTION

Use the `Update-SPRepopulateMicroblogFeedCache` cmdlet to refresh the feeds of a given user.
It can be used in scenarios where the automatic refresh has failed or when reverting to an old version of a user's personal site.

When you refresh the cache, the `Update-SPRepopulateMicroblogLMTCache` cmdlet should be run first and then the `Update-SPRepopulateMicroblogFeedCache` cmdlet second.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE 1

```powershell
$proxy = Get-SPServiceApplicationProxy | ?{$_.TypeName -eq 'User Profile Service Application Proxy'}
Update-SPRepopulateMicroblogFeedCache -ProfileServiceApplicationProxy $proxy -AccountName contoso\userName
```

This example refreshes the feed for a specific user by using the AccountName parameter.

### EXAMPLE 2

```powershell
$site = (Get-SPWebApplication -IncludeCentralAdministration | ?{$_.IsAdministrationWebApplication -eq $true}).Sites[0]
$context = Get-SPServiceContext $site
$upm = New-Object Microsoft.Office.Server.UserProfiles.UserProfileManager($context)
$profiles = $upm.GetEnumerator()
$proxy = Get-SPServiceApplicationProxy | ?{$_.TypeName -eq 'User Profile Service Application Proxy'}
while($profiles.MoveNext()) {
    $profile = $profiles.Current
    Update-SPRepopulateMicroblogFeedCache -ProfileServiceApplicationProxy $proxy -AccountName $profile.AccountName }
```

This example refreshes the feeds for all users in the User Profile Service Application.

### EXAMPLE 3

```powershell
Update-SPRepopulateMicroblogFeedCache -ProfileServiceApplicationProxy $proxy -SiteUrl https://sharepoint.contoso.com
```

This example refreshes the feed on the site https://sharepoint.contoso.com.

## PARAMETERS

### -AccountName

> Applicable: SharePoint Server Subscription Edition

Specifies the user's account name for the User Profile Service application.

```yaml
Type: String
Parameter Sets: (All), Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProfileServiceApplicationProxy

> Applicable: SharePoint Server Subscription Edition

Specifies the User Profile Service application proxy to update.

The type must be in one of the following forms:

--A valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh
--A valid name of a service application proxy (for example, UserProfileSvcProxy1)
--An instance of a valid SPServiceApplicationProxy object

```yaml
Type: SPServiceApplicationProxyPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -SiteSubscription

> Applicable: SharePoint Server Subscription Edition

Specifies the account under which this service should run.
This parameter is mandatory in a hosted-environment and optional in a non-hosted environment.

```yaml
Type: SPSiteSubscriptionPipeBind
Parameter Sets: (All), Default, FollowableList
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteUrl

> Applicable: SharePoint Server Subscription Edition

Specifies the Site's URL to repopulate the site feeds. If you don't specify this parameter, you must specify the AccountName parameter. If neither parameter is specified, an error message is displayed.

```yaml
Type: String
Parameter Sets: (All), Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ListId

> Applicable: SharePoint Server Subscription Edition

The ListId of the FollowableList.

```yaml
Type: Guid
Parameter Sets: FollowableList
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ListRootFolderUrl

> Applicable: SharePoint Server Subscription Edition

The RootFolderUrl of the FollowableList.

```yaml
Type: String
Parameter Sets: FollowableList
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteId

> Applicable: SharePoint Server Subscription Edition

The SiteId containing the FollowableList.

```yaml
Type: Guid
Parameter Sets: FollowableList
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebId

> Applicable: SharePoint Server Subscription Edition

The WebId containing the FollowableList.

```yaml
Type: Guid
Parameter Sets: FollowableList
Aliases:

Required: True
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

[Update-SPRepopulateMicroblogLMTCache](Update-SPRepopulateMicroblogLMTCache.md)
