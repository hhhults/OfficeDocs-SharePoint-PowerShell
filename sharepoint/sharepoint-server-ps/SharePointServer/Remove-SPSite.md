---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/remove-spsite
applicable: SharePoint Server Subscription Edition
title: Remove-SPSite
schema: 2.0.0
---

# Remove-SPSite

## SYNOPSIS
Completely deletes an existing site collection and all subsites.

## SYNTAX

```
Remove-SPSite  [-Identity] <SPSitePipeBind> [-DeleteADAccounts] [-GradualDelete]
 [-CheckComplianceFlags <Boolean>] [-AssignmentCollection <SPAssignmentCollection>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Remove-SPSite** cmdlet completely deletes an existing site collection and all subsites.
This operation cannot be undone.

## EXAMPLES

### EXAMPLE 1
```powershell
Remove-SPSite -Identity 'https://sitename' -GradualDelete -Confirm:$False
```

This example removes the given site collection and all included sites by using GradualDelete which places the site in the site recycle bin; confirmation has been suppressed.

### EXAMPLE 2
```powershell
Remove-SPSite -Identity 'https://sitename'
```

This example immediately deletes the site and it's contents from the farm.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the identity of the site to delete.
The identity can be either a valid URL, in the form https://server_name; a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; or an SPSite object.

```yaml
Type: SPSitePipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DeleteADAccounts

> Applicable: SharePoint Server Subscription Edition

Forces deletion of user accounts from Active Directory Domain Services (AD DS).
This applies when in AD DS account creation mode and the value of this parameter is True, AD DS accounts associated with the site collection are also deleted from AD DS.

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

### -CheckComplianceFlags

> Applicable: SharePoint Server Subscription Edition

Specifies if compliance flags are enabled.

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

### -AssignmentCollection

> Applicable: SharePoint Server Subscription Edition

Manages objects for the purpose of proper disposal. Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

When the Global parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the `Stop-SPAssignment` command, an out-of-memory scenario can occur.

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

### -DeleteADAccounts

> Applicable: SharePoint Server Subscription Edition

Forces deletion of user accounts from Active Directory Domain Services (AD DS).

This applies when in AD DS account creation mode and the value of this parameter is True, AD DS accounts associated with the site collection are also deleted from AD DS.

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

### -GradualDelete

> Applicable: SharePoint Server Subscription Edition

If provided, occurs gradually to use less system load.

This operation is strongly recommended for deleting very large sites. This option places the site in the site recycle bin instead of immediately deleting the site.

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
