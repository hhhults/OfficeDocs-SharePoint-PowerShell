---
external help file: Microsoft.SharePoint.PowerShell.SSOUpgrade-help.xml
Module Name: Microsoft.SharePoint.Powershell
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/update-spsecurestoremasterkey
applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019
title: Update-SPSecureStoreMasterKey
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# Update-SPSecureStoreMasterKey

## SYNOPSIS
Changes the master key of a Secure Store Service application.

## SYNTAX

```
Update-SPSecureStoreMasterKey -Passphrase <String> -ServiceApplicationProxy <SPServiceApplicationProxyPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [<CommonParameters>]
```

## DESCRIPTION
The `Update-SPSecureStoreApplicationServerKey` cmdlet changes the master key of a Secure Store Service application.

Updating the master key is required when:

--A new instance of a service application is created and the database for the Secure Store service application is new or empty.

--The master key or passphrase has been compromised.

--Security guidelines require that the passphrase or key be replaced.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```
$newPassPhrase = "abcDEF123!"
$proxy = Get-SPServiceApplicationProxy | ?{$_.TypeName -eq 'Secure Store Service Application Proxy'}
Update-SPSecureStoreMasterKey -ServiceApplicationProxy $proxy -Passphrase $newPassPhrase
```

This example creates a new master key for the given service application.

## PARAMETERS

### -Passphrase

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the passphrase that is used for the Secure Store database.
The passphrase that you enter is not stored.
Make sure that you write down the passphrase and store it in a secure location.
The passphrase will be required to add new Secure Store service servers.

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

### -ServiceApplicationProxy

> Applicable: SharePoint Server 2010, SharePoint Server 2013, SharePoint Server 2016, SharePoint Server 2019

Specifies the proxy of the Secure Store service application that contains the master key to update.

```yaml
Type: SPServiceApplicationProxyPipeBind
Parameter Sets: (All)
Aliases:

Required: True
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
