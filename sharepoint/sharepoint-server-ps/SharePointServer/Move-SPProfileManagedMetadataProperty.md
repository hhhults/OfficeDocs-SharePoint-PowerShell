---
external help file: Microsoft.Office.Server.UserProfiles.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/move-spprofilemanagedmetadataproperty
applicable: SharePoint Server Subscription Edition
title: Move-SPProfileManagedMetadataProperty
schema: 2.0.0
---

# Move-SPProfileManagedMetadataProperty

## SYNOPSIS
Moves multiple-string values into a term set.

## SYNTAX

```
Move-SPProfileManagedMetadataProperty -Identity <String>
 -ProfileServiceApplicationProxy <SPServiceApplicationProxyPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-AvailableForTagging] [-Confirm] [-TermSetName <String>]
 [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
Use the Move-SPProfileManagedMetadataProperty cmdlet to move multiple-string or single-string property values into a term set that you specify.
If you do not specify a term set, the values are moved into the Keywords term set.
Any new values you add to the property after running the cmdlet will be moved into the term set that you specified.

After a user profile application has been upgraded from Office SharePoint Server, single-string and multiple-string value properties are not available for use unless the Move-SPProfileManagedMetadataProperty cmdlet is run to map them to term sets within Managed Metadata Service.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
$proxy = Get-SPServiceApplicationProxy | ?{$_.TypeName -eq 'User Profile Service Application Proxy'}
Move-SPProfileManagedMetadataProperty -ProfileServiceApplicationProxy $proxy -Identity SPS-Interests -TermSetName Interests -AvailableForTagging
```

This example moves values from the SPS-Interests property into a new term set called Interests and marks that term set as available for tagging.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the profile property that needs to be migrated to the taxonomy.

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

### -ProfileServiceApplicationProxy

> Applicable: SharePoint Server Subscription Edition

Specifies the name of the User Profile Service Application Proxy to use.

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

### -AvailableForTagging

> Applicable: SharePoint Server Subscription Edition

Determines whether the terms in the resulting term set can be used for Managed Metadata tagging.
If a term set has more than 30,000 terms, using it for Managed Metadata tagging may lead to performance issues on the client computer.
Because a majority of the profile properties may have more than 30,000 terms, the default value is No.

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

### -TermSetName

> Applicable: SharePoint Server Subscription Edition

When specified, the term set name is created.
If the TermSetName parameter is not specified, the property is mapped to the Keywords term set in Managed Metadata Service.

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
