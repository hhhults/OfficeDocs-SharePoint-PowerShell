---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-spthrottlingrule
applicable: SharePoint Server Subscription Edition
title: Set-SPThrottlingRule
schema: 2.0.0
---

# Set-SPThrottlingRule

## SYNOPSIS
Changes properties of an existing throttling rule.

## SYNTAX

```
Set-SPThrottlingRule [-Identity] <SPThrottlingRulePipeBind> [-AssignmentCollection <SPAssignmentCollection>]
 [-Criteria <SPRequestManagementRuleCriteriaPipeBind[]>] [-Expiration <DateTime>] [-Threshold <Int32>]
 [<CommonParameters>]
```

## DESCRIPTION
Use the `Set-SPThrottlingRule` cmdlet to change the properties of an existing throttling rule by using the Identity parameter.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
$web=Get-SPWebApplication -Identity <URL of web application>
$rm=Get-SPRequestManagementSettings -Identity $web
$c=New-SPRequestManagementRuleCriteria -Value http -Property url -MatchType startswith -CaseSensitive $false
$throttlingrule=Add-SPThrottlingRule -RequestManagementSettings $rm -Name <Rule Name> -Criteria $c -Threshold 4
$criteriaNew = New-SPRequestManagementRuleCriteria -Property UserAgent -MatchType Equals -Value "Mozilla/4.0 (compatible; MSIE 4.01; Windows NT; MS Search 6.0 Robot)"
Set-SPThrottlingRule -Identity $ throttlingrule -Criteria $criteriaNew -Threshold 8
```

This example sets throttling rule property

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the throttling rule object to set.

```yaml
Type: SPThrottlingRulePipeBind
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

### -Criteria

> Applicable: SharePoint Server Subscription Edition

Specifies the criteria for the rule to match.

```yaml
Type: SPRequestManagementRuleCriteriaPipeBind[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Expiration

> Applicable: SharePoint Server Subscription Edition

Specifies the expiration date and time of the rule.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Threshold

> Applicable: SharePoint Server Subscription Edition

Specifies a value between 0 and 10 which defines the maximum threshold for throttling.
The Request Manager will remove routing targets if the Health-Score becomes greater than this value.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-SPThrottlingRule](Add-SPThrottlingRule.md)

[Get-SPThrottlingRule](Get-SPThrottlingRule.md)

[Remove-SPThrottlingRule](Remove-SPThrottlingRule.md)
