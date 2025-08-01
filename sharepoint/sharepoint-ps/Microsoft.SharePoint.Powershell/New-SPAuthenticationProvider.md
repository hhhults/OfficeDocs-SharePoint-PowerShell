---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
Module Name: Microsoft.SharePoint.Powershell
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/new-spauthenticationprovider
applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019
title: New-SPAuthenticationProvider
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# New-SPAuthenticationProvider

## SYNOPSIS

Creates a new authentication provider in the farm.


## SYNTAX

### Forms
```
New-SPAuthenticationProvider -ASPNETMembershipProvider <String> -ASPNETRoleProviderName <String>
 [-AssignmentCollection <SPAssignmentCollection>] [<CommonParameters>]
```

### Trusted
```
New-SPAuthenticationProvider -TrustedIdentityTokenIssuer <SPTrustedIdentityTokenIssuerPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [<CommonParameters>]
```

### Windows
```
New-SPAuthenticationProvider [-AllowAnonymous] [-AssignmentCollection <SPAssignmentCollection>]
 [-DisableKerberos] [-UseBasicAuthentication] [-UseWindowsIntegratedAuthentication] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet contains more than one parameter set.
You may only use parameters from one parameter set, and you may not combine parameters from different parameter sets.
For more information about how to use parameter sets, see [Cmdlet parameter sets](https://learn.microsoft.com/powershell/scripting/developer/cmdlet/cmdlet-parameter-sets).

The New-SPAuthenticationProvider cmdlet creates a new authentication provider in the farm.

--NTLM, Classic NTLM, Negotiate, and Classic Negotiate can be set only in a web application.
--For ASP.NET Membership Provider or Role providers, no objects are persisted. The object is created and used for setting this type of Authentication provider in a web application.
--For STS Authentication providers, an object is created and persisted in the SPFarm object.

You cannot use classic NTLM with any claims-based authentication type.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### ---------------------------EXAMPLE1------------------
```
$ap = New-SPAuthenticationProvider -UseWindowsIntegratedAuthentication
Set-SPWebApplication -Name "Claims Windows Web App" -ApplicationPool "Claims App Pool" -ApplicationPoolAccount "redmond\appool" -Url http://<servername> -Port 80 -AuthenticationProvider $ap
```

This example creates a Windows claims authentication provider.

### ---------------------------EXAMPLE2------------------
```
$ap = New-SPAuthenticationProvider -ASPNETMembershipProvider "membership" -ASPNETRoleProviderName "rolemanager"
Set-SPWebApplication -Name "Claims Windows Web App" -ApplicationPool "Claims App Pool" -ApplicationPoolAccount "redmond\appool" -Url http://<servername> -Port 80 -AuthenticationProvider $ap
```

This example creates an authentication provider that is based on the ASP.NET membership role provider.

### ---------------------------EXAMPLE3------------------
```
$ap = New-SPAuthenticationProvider -TrustedIdentityTokenIssuer | Get-SPTrustedIdentityTokenIssuer "LiveIDSTS"
Set-SPWebApplication -Name "Claims Windows Web App" -ApplicationPool "Claims App Pool" -ApplicationPoolAccount "redmond\appool" -Url http://<servername> -Port 80 -AuthenticationProvider $ap
```

This example creates a trusted token issuer authentication provider.

## PARAMETERS

### -ASPNETMembershipProvider

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the name of the membership provider.

The value must be a valid name of an ASP.NET membership provider; for example, myMembershipProvider.

```yaml
Type: String
Parameter Sets: Forms
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ASPNETRoleProviderName

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the name of the role provider.

The value must be a valid name of an ASP.NET role provider; for example, myRoleProvider.

```yaml
Type: String
Parameter Sets: Forms
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrustedIdentityTokenIssuer

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the identity of the authentication provider.

The value must be in one of the following forms:

--A valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh
--A valid name of a TrustedIdentityTokenIssuer (for example, myRoleProvider)
--An instance of a valid SPTrustedIdentityTokenIssuer object

```yaml
Type: SPTrustedIdentityTokenIssuerPipeBind
Parameter Sets: Trusted
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowAnonymous

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies whether the web application allows anonymous access.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AssignmentCollection

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

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

### -DisableKerberos

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies whether the web application disables Kerberos authentication.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseBasicAuthentication

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies whether the web application uses Basic authentication.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseWindowsIntegratedAuthentication

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies whether the web application uses Integrated Windows authentication.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
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
