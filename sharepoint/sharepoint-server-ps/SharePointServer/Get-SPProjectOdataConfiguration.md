---
external help file: microsoft.office.project.server.stsadmcommandhandler.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/get-spprojectodataconfiguration

title: Get-SPProjectOdataConfiguration
schema: 2.0.0
---

# Get-SPProjectOdataConfiguration

## SYNOPSIS
Returns the settings for how the OData service is configured for an instance of Project Web App.

## SYNTAX

```
Get-SPProjectOdataConfiguration [-AssignmentCollection <SPAssignmentCollection>] [<CommonParameters>]
```

## DESCRIPTION
The Get-SPProjectOdataConfiguration cmdlet returns the settings for how the OData service is configured for an instance of Project Web App.
It returns the current settings for a list of parameters that specify paging, the enabling of various querying functionality, whether MaxResultsPerCollection has been enabled, and whether verbose errors are enabled.
The cmdlet can also be used to return an itemized list of entities that have an override specified for their maximum page size.

For permissions and the most current information about Windows PowerShell for Project Server, see the online documentation at https://go.microsoft.com/fwlink/p/?LinkId=251833 (https://go.microsoft.com/fwlink/p/?LinkId=251833).

## EXAMPLES

### EXAMPLE 1
```powershell
Get-SPProjectOdataConfiguration
```

This example returns the OData configuration for the instance of Project Web App.

### EXAMPLE 2
```powershell
(Get-SPProjectOdataConfiguration).EntitySetsWithMaxPAgeSizeOverride
```

This example returns the list of entities that have the MaxPageSizeOverride option configured.

## PARAMETERS

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
