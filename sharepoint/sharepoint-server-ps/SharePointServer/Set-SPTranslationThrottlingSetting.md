---
external help file: Microsoft.SharePoint.Translation.dll-Help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-sptranslationthrottlingsetting
applicable: SharePoint Server Subscription Edition
title: Set-SPTranslationThrottlingSetting
schema: 2.0.0
---

# Set-SPTranslationThrottlingSetting

## SYNOPSIS
Sets the timer job duration.

## SYNTAX

```
Set-SPTranslationThrottlingSetting [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 [-SiteQuota <Int32>] [-TenantQuota <Int32>] [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION
Use the Set-SPTranslationThrottlingSetting cmdlet to set the timer job duration for each site collection.

## EXAMPLES

### EXAMPLE
```powershell
Set-SPTranslationThrottlingSetting -SiteQuota 300 -TenantQuota 600
```

This limits the Translation Timer job to spend no more than 300 seconds (5 minutes) per site collection, and no more than 600 seconds (10 minutes) per tenant.

Note: TenantQuota must be greater than or equal to SiteQuota.

## PARAMETERS

### -AssignmentCollection

> Applicable: SharePoint Server Subscription Edition

Manages objects for the purpose of proper disposal. Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

**NOTE:** When the Global parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the Stop-SPAssignment command, an out-of-memory scenario can occur.

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

Prompts you for confirmation before running the cmdlet.

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

### -SiteQuota

> Applicable: SharePoint Server Subscription Edition

The duration (in seconds) of timer job processing time that an individual SPSite is limited to

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

### -TenantQuota

> Applicable: SharePoint Server Subscription Edition

The duration (in seconds) of timer job processing time that an individual tenant is limited to.

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

### -WhatIf

> Applicable: SharePoint Server Subscription Edition

Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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

### Microsoft.SharePoint.PowerShell.SPAssignmentCollection

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
