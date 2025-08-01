---
external help file: Microsoft.Office.Server.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/export-spserverscaleoutdatabasetenantdata
applicable: SharePoint Server Subscription Edition
title: Export-SPServerScaleOutDatabaseTenantData
schema: 2.0.0
---

# Export-SPServerScaleOutDatabaseTenantData

## SYNOPSIS

Exports the data of the specified subscription.

## SYNTAX

```
Export-SPServerScaleOutDatabaseTenantData [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 -FilePath <String> [-Force] -ServiceApplication <SPServiceApplicationPipeBind> -SiteSubscriptionId <Guid>
 [-WhatIf] [<CommonParameters>]
```

## DESCRIPTION

Use the Export-SPServerScaleOutDatabaseTenantData cmdlet to export the data of the specified subscription id to the specified file from the specified service application.

## EXAMPLES

### EXAMPLE
```powershell
Export-SPServerScaleOutDatabaseTenantData -FilePath "C:\TenantData.dat" -ServiceApplication $serviceApplication -SiteSubscriptionId "5CAF2F99-A75F-4239-B9CD-7FE63D1CE904"
```

This example exports data for the site subscription with id 5CAF2F99-A75F-4239-B9CD-7FE63D1CE904 to the file at C:\ TenantData.dat, from the specified service application.

## PARAMETERS

### -AssignmentCollection

> Applicable: SharePoint Server Subscription Edition

{{Fill AssignmentCollection Description}}

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

### -FilePath

> Applicable: SharePoint Server Subscription Edition

{{Fill FilePath Description}}

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

### -Force

> Applicable: SharePoint Server Subscription Edition

{{Fill Force Description}}

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

### -ServiceApplication

> Applicable: SharePoint Server Subscription Edition

{{Fill ServiceApplication Description}}

```yaml
Type: SPServiceApplicationPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSubscriptionId

> Applicable: SharePoint Server Subscription Edition

{{Fill SiteSubscriptionId Description}}

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
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

[Clear-SPServerScaleOutDatabaseTenantData](Clear-SPServerScaleOutDatabaseTenantData.md)

[Import-SPServerScaleOutDatabaseTenantData](Import-SPServerScaleOutDatabaseTenantData.md)
