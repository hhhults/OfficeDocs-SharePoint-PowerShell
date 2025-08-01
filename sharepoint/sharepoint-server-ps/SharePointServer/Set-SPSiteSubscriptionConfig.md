---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-spsitesubscriptionconfig
applicable: SharePoint Server Subscription Edition
title: Set-SPSiteSubscriptionConfig
schema: 2.0.0
---

# Set-SPSiteSubscriptionConfig

## SYNOPSIS
Sets the configuration properties of a site subscription.

## SYNTAX

```
Set-SPSiteSubscriptionConfig [-Identity] <SPSiteSubscriptionPipeBind>
 [-AssignmentCollection <SPAssignmentCollection>] [-Confirm] [-PassThru] [-UserAccountDirectoryPath <String>]
 [-WhatIf] [-FeaturePack <SPSiteSubscriptionFeaturePackPipeBind>] [<CommonParameters>]
```

## DESCRIPTION
The `Set-SPSiteSubscriptionConfig` cmdlet sets the configuration properties of a site subscription.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
Set-SPSiteSubscriptionConfig https://contoso.com -FeaturePack 12345678-90ab-cdef-1234-567890abcdef
```

This example sets the Feature set of the entire site subscription that contains https://contoso.com with a Feature pack GUID.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the site subscription configuration to update.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; an SPSite (object or URL) of a site collection that is a member of the site subscription; or an instance of a valid SiteSubscription object.

```yaml
Type: SPSiteSubscriptionPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
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

### -PassThru

> Applicable: SharePoint Server Subscription Edition

Specifies the output object can be passed through the pipeline.

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

### -UserAccountDirectoryPath

> Applicable: SharePoint Server Subscription Edition

Sets the site user account directory path to a specific organizational unit (OU) that is in the same domain as the site subscription.

The type must be a name of a distinguished OU; for example, OU=Contoso1, DC=OSGCorp,DC=local.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -FeaturePack

> Applicable: SharePoint Server Subscription Edition

{{Fill FeaturePack Description}}

```yaml
Type: SPSiteSubscriptionFeaturePackPipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
