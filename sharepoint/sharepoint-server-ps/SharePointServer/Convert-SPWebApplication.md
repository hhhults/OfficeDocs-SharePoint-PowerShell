---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/convert-spwebapplication
applicable: SharePoint Server Subscription Edition
title: Convert-SPWebApplication
schema: 2.0.0
---

# Convert-SPWebApplication

## SYNOPSIS

Converts the authentication mode of a web application.


## SYNTAX

```
Convert-SPWebApplication -Identity <SPWebApplicationPipeBind> -From <String> -To <String>
 [-AssignmentCollection <SPAssignmentCollection>] [-Force] [-RetainPermissions] [-Database <SPContentDatabase>]
 [-MapList <String>] [-SiteSubsriptionId <Guid>] [-SkipPolicies] [-SkipSites]
 [-SourceSkipList <String>] [-TrustedProvider <SPTrustedIdentityTokenIssuerPipeBind>]
 [-LoggingDirectory <String>] [<CommonParameters>]
```

## DESCRIPTION
Use the Convert-SPWebApplication cmdlet to convert the authentication mode of a Web application to Windows Claims authentication mode and migrate the user accounts in the content database to claims encoded values.

When retaining permissions, users within Sites are only converted if the source account is enabled and queryable by SharePoint. For example, if the Active Directory account is deleted or disabled prior to a Classic Windows to Windows Claims conversion, the account in the database will not be updated to the Claims format.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE 1
```powershell
Convert-SPWebApplication -Identity "https://<webappurl>" -To Claims -RetainPermissions
```

This example converts a web application specified by the Identity parameter to use the claim authentication mode.

### EXAMPLE 2
```powershell
Convert-SPWebApplication -Identity "https://<webappurl>" -From Legacy -To Claims -RetainPermissions
```

This example converts a web application specified by the Identity parameter from Classic Windows authentication to Claims authentication mode while retaining permissions. The -From parameter is required after security update MS04-022 or the April 2014 Cumulative Update for SharePoint Server 2013 is applied. This is required for all versions of SharePoint Server 2016.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the URL of the web application that you want to convert, for example: https://mysite/app1

```yaml
Type: SPWebApplicationPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -From

> Applicable: SharePoint Server Subscription Edition

Specifies the authentication method to convert from.

Valid values for this parameter are as follows.

Legacy, Claims-Windows, Claims-Trusted-Default

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -To

> Applicable: SharePoint Server Subscription Edition

Specifies the authentication method to convert to.

Valid values for this parameter are as follows.

Claims, Claims-Windows, Claims-Trusted-Default, Claims-SharePoint-Online

```yaml
Type: String
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

### -Force

> Applicable: SharePoint Server Subscription Edition

Forces the conversion of the web application.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetainPermissions

> Applicable: SharePoint Server Subscription Edition

Specifies the account under which the cmdlet is run and retains the permission in the web application.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Database

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the content database to migrate.

```yaml
Type: SPContentDatabase
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MapList

> Applicable: SharePoint Server Subscription Edition

Specifies a file containing as list of rows in the following format: user-key, migrated-user-name, migrated-user-key.

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

### -SiteSubsriptionId

> Applicable: SharePoint Server Subscription Edition

Specifies the GUID fo the Site Subscription.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipPolicies

> Applicable: SharePoint Server Subscription Edition

Specifies the SPWebApplication security policies will not be migrated.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipSites

> Applicable: SharePoint Server Subscription Edition

Specifies the SPWebApplication's SPSites will not be migrated.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceSkipList

> Applicable: SharePoint Server Subscription Edition

Specifies a file containing as list of rows in the following format: user-key.

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

### -TrustedProvider

> Applicable: SharePoint Server Subscription Edition

When you migrate from a trusted login provider this is how you specify which trusted login provider.

```yaml
Type: SPTrustedIdentityTokenIssuerPipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LoggingDirectory

> Applicable: SharePoint Server Subscription Edition

Specifies a directory where verbose logs about the results of the migration will be written.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
