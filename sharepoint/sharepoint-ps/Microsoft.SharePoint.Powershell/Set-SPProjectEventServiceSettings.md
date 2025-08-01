---
external help file: microsoft.office.project.server.stsadmcommandhandler.dll-help.xml
Module Name: Microsoft.SharePoint.Powershell
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/set-spprojecteventservicesettings
applicable: Project Server 2016, Project Server 2019
title: Set-SPProjectEventServiceSettings
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# Set-SPProjectEventServiceSettings

## SYNOPSIS
Allows you to change the Microsoft Project Server Events Service 2016 TCP port settings. If you change the TCP port, the Microsoft Project Server Events Service 2016 needs to be restarted for the changes to take effect.

## SYNTAX

```
Set-SPProjectEventServiceSettings [-AssignmentCollection <SPAssignmentCollection>] [-NetTcpPort <Int32>]
 [<CommonParameters>]
```

## DESCRIPTION
Allows you to change the Microsoft Project Server Events Service 2016 TCP port settings. If you change the TCP port, the Microsoft Project Server Events Service 2016 needs to be restarted for the changes to take effect.

## EXAMPLES

### EXAMPLE
```
Set-SPProjectEventServiceSettings -NetTcpPort 16100
```

This example tells the service to listen on port 16100.

## PARAMETERS

### -AssignmentCollection

> Applicable: Project Server 2016, Project Server 2019

Manages objects for the purpose of proper disposal. Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management. Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory. When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

When the Global parameter is used, all objects are contained in the global store. If objects are not immediately used, or disposed of by using the Stop-SPAssignment command, an out-of-memory scenario can occur.

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

### -NetTcpPort

> Applicable: Project Server 2016, Project Server 2019

TCP port to listen on.

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

### Microsoft.SharePoint.PowerShell.SPAssignmentCollection

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
