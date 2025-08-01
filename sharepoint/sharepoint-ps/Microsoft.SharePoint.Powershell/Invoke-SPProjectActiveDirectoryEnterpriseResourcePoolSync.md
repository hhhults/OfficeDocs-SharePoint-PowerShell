---
external help file: microsoft.office.project.server.stsadmcommandhandler.dll-help.xml
Module Name: Microsoft.SharePoint.Powershell
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/invoke-spprojectactivedirectoryenterpriseresourcepoolsync
applicable: Project Server 2013, Project Server 2016, Project Server 2019
title: Invoke-SPProjectActiveDirectoryEnterpriseResourcePoolSync
schema: 2.0.0
author: techwriter40
ms.author: pamgreen
ms.reviewer:
---

# Invoke-SPProjectActiveDirectoryEnterpriseResourcePoolSync

## SYNOPSIS
Triggers Active Directory Enterprise Resource Pool synchronization on the specified instance of Project Web App.

## SYNTAX

```
Invoke-SPProjectActiveDirectoryEnterpriseResourcePoolSync [-Url] <Uri>
 [-AssignmentCollection <SPAssignmentCollection>] [<CommonParameters>]
```

## DESCRIPTION
Active Directory Enterprise Resource Pool synchronization is used to create or update multiple Project Server enterprise resources at the same time.
Project Server enterprise resources can also be automatically activated and deactivated based on group membership in the Active Directory directory service.
For example, new employees in your department can automatically be added as Project Server enterprise resources as long as they are in the Active Directory group selected for synchronization.
Conversely, employees who are removed from the Active Directory group have their Project Server accounts deactivated upon synchronization.

Enterprise Resource Pool synchronization also updates enterprise resource properties with the most current data from Active Directory.
For example, an employee's name and e-mail address may change because of marriage.
As long as the change is made in Active Directory and the user is in the linked group, the change occurs in the user's Enterprise Resource properties when synchronization occurs.

The Enterprise Resource Pool can be mapped to a single Active Directory group for synchronization.
However, this Active Directory group can contain nested groups whose members are also synchronized.

The following actions can occur during the Enterprise Resource Pool synchronization process:

- A new Project Server enterprise resource and corresponding user account can be created based on an Active Directory account.
- An active Project Server resource/user account can be deactivated.
- An existing Project Server user account's metadata (for example, name, e-mail address, and so on) can be updated if it has changed in Active Directory.
- A previously inactive Project Server resource/user account can be reactivated.

For permissions and the most current information about Windows PowerShell for Project Server, see the online documentation at https://go.microsoft.com/fwlink/p/?LinkId=251833 (https://go.microsoft.com/fwlink/p/?LinkId=251833).

## EXAMPLES

### EXAMPLE
```
Invoke-SPProjectActiveDirectoryEnterpriseResourcePoolSync https://localhost/pwa
```

This example triggers an Active Directory Enterprise Resource Pool synchronization for the instance of Project Web App located at https://localhost/pwa.

## PARAMETERS

### -Url

> Applicable: Project Server 2013, Project Server 2016, Project Server 2019

Specifies the URL of the Project Web App instance where you want to invoke a synchronization.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AssignmentCollection

> Applicable: Project Server 2013, Project Server 2016, Project Server 2019

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Disable-SPProjectActiveDirectoryEnterpriseResourcePoolSync](Disable-SPProjectActiveDirectoryEnterpriseResourcePoolSync.md)
