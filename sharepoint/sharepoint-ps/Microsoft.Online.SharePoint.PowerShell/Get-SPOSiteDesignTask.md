---
external help file: Microsoft.Online.SharePoint.PowerShell.dll-Help.xml
Module Name: Microsoft.Online.SharePoint.PowerShell
online version: https://learn.microsoft.com/powershell/module/sharepoint-online/get-spositedesigntask
applicable: SharePoint Online
title: Get-SPOSiteDesignTask
schema: 2.0.0
author: trent-green
ms.author: trgreen
ms.reviewer:
---

# Get-SPOSiteDesignTask

## SYNOPSIS

Cmdlet to get a scheduled site design script.

## SYNTAX

```
Get-SPOSiteDesignTask [[-Identity] <SPOSiteDesignTaskPipeBind>] [[-WebUrl] <String>] [<CommonParameters>]
```

## DESCRIPTION

Used to retrieve a scheduled site design script. It takes the ID of the scheduled site design and the URL fo the SPWeb where the site design is scheduled to be applied.

> [!NOTE]
> This command only retrieves a previously scheduled request.

## EXAMPLES

### EXAMPLE 1

```powershell
Get-SPOSiteDesignTask -Identity 501z8c32-4147-44d4-8607-26c2f67cae82 -WebUrl "https://contoso.sharepoint.com/sites/projectawesome"
```

This example returns a scheduled site design whose ID is 501z8c32-4147-44d4-8607-26c2f67cae82 and which was applied on the site <https://contoso.sharepoint.com/sites/projectawesome>.

## PARAMETERS

### -Identity

> Applicable: SharePoint Online

The ID of the scheduled site design to apply.

```yaml
Type: Microsoft.Online.SharePoint.PowerShell.SPOSiteDesignTaskPipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebUrl

> Applicable: SharePoint Online

The URL of the site collection where the site design will be applied.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

### Microsoft.Online.SharePoint.PowerShell.SPOSiteDesignTaskPipeBind

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Add-SPOSiteDesignTask](Add-SPOSiteDesignTask.md)

[Get-SPOSiteDesignRun](Get-SPOSiteDesignRun.md)

[Get-SPOSiteDesignRunStatus](Get-SPOSiteDesignRunStatus.md)
