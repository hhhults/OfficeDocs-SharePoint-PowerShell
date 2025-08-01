---
external help file: Microsoft.SharePoint.PowerShell.dll-help.xml
module name: SharePointServer
online version: https://learn.microsoft.com/powershell/module/sharepoint-server/update-spsolution
applicable: SharePoint Server Subscription Edition
title: Update-SPSolution
schema: 2.0.0
---

# Update-SPSolution

## SYNOPSIS
Upgrades a deployed SharePoint solution.

## SYNTAX

```
Update-SPSolution [-Identity] <SPSolutionPipeBind> -LiteralPath <String>
 [-AssignmentCollection <SPAssignmentCollection>] [-CASPolicies] [-Confirm] [-Force] [-GACDeployment] [-Local]
 [-Time <String>] [-WhatIf] [-FullTrustBinDeployment] [<CommonParameters>]
```

## DESCRIPTION
The `Update-SPSolution` cmdlet upgrades a deployed SharePoint solution in the farm.
Use this cmdlet only if a new solution contains the same set of files and features as the deployed solution.
If files and features are different, the solution must be retracted and redeployed by using the `Uninstall-SPSolution` and `Install-SPSolution` cmdlets, respectively.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at [SharePoint Server Cmdlets](https://learn.microsoft.com/powershell/sharepoint/sharepoint-server/sharepoint-server-cmdlets).

## EXAMPLES

### EXAMPLE
```powershell
Update-SPSolution -Identity contoso_solution.wsp -LiteralPath c:\contoso_solution_v2.wsp -GACDeployment
```

This example upgrades the deployed SharePoint solution  contoso_solution.wsp to the solution c:\contoso_solution_v2.wsp.

## PARAMETERS

### -Identity

> Applicable: SharePoint Server Subscription Edition

Specifies the SharePoint solution to deploy.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a SharePoint solution (for example, SPSolution1); or an instance of a valid SPSolution object.

```yaml
Type: SPSolutionPipeBind
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LiteralPath

> Applicable: SharePoint Server Subscription Edition

Specifies the path to the solution package.

The type must be a valid path in either of the following forms:

- C:\folder_name
- \\\\server_name\folder_name

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

### -CASPolicies

> Applicable: SharePoint Server Subscription Edition

Specifies that Code Access Security (CAS) policies can be deployed for the new SharePoint solution.

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

### -Force

> Applicable: SharePoint Server Subscription Edition

Forces the deployment of the new SharePoint solution.

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

### -GACDeployment

> Applicable: SharePoint Server Subscription Edition

Specifies that the new SharePoint solution can be deployed to the global assembly cache (GAC).

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

### -Local

> Applicable: SharePoint Server Subscription Edition

Deploys the solution on the local computer only.

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

### -Time

> Applicable: SharePoint Server Subscription Edition

Specifies when the solution will be deployed.
The default value is immediate deployment.

The type must be a valid DateTime value, in the form 2010, 5, 1.

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

### -FullTrustBinDeployment

> Applicable: SharePoint Server Subscription Edition

Specifies whether to deploy using fully trusted bin.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
