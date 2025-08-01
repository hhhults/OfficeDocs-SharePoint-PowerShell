---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/new-spclaimtypemapping
applicable: SharePoint Server Subscription Edition
title: New-SPClaimTypeMapping
schema: 2.0.0
---

# New-SPClaimTypeMapping

## SYNOPSIS

Creates a claim mapping rule for a security token service (STS) identity provider.

## SYNTAX

```
New-SPClaimTypeMapping [-IncomingClaimType] <String> [-IncomingClaimTypeDisplayName] <String>
 [[-LocalClaimType] <String>] [-AssignmentCollection <SPAssignmentCollection>] [-SameAsIncoming]
 [<CommonParameters>]
```

## DESCRIPTION
The New-SPClaimTypeMapping cmdlet creates a claim mapping rule for a security token service (STS) identity provider.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE 1
```powershell
$map1 = New-SPClaimTypeMapping -IncomingClaimType "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/emailaddress" -IncomingClaimTypeDisplayName "EmailAddress" -SameAsIncoming
$map2 = New-SPClaimTypeMapping -IncomingClaimType "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/nameidentifier" -IncomingClaimTypeDisplayName "PUID" -LocalClaimType "http://schemas.xmlsoap.org/ws/2005/05/identity/claims/thumbprint"
New-SPTrustedIdentityTokenIssuer -Name "LiveIDSTS" -Description "LiveID Provider" -Realm "urn:domain.company.com" -ImportTrustCertificate $cert -ClaimsMappings $map1[,$map2..] -SignInUrl "https://login.live.com/login.srf" -IdentifierClaim $map2.InputClaimType
```

This example creates a claim map from an incoming token to a SharePoint token.

## PARAMETERS

### -IncomingClaimType

> Applicable: SharePoint Server Subscription Edition

Specifies the URI of the incoming claim type.

The type must be a valid URI, in the form http://schemas.microsoft.com/email.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncomingClaimTypeDisplayName

> Applicable: SharePoint Server Subscription Edition

Specifies the display name of the incoming claim type.

The type must be a valid name of an incoming claim type; for example, Email.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalClaimType

> Applicable: SharePoint Server Subscription Edition

Specifies the URI of the local claim type.
If the SameAsIncoming parameter is False, this is a required parameter.

The type must be a valid URI, in the form http://schemas.microsoft.com/email.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
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

### -SameAsIncoming

> Applicable: SharePoint Server Subscription Edition

Specifies that the claim type specified in the IncomingClaimType parameter is used for the LocalClaimType parameter.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
