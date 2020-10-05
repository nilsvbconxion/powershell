---
applicable: SharePoint Online
external help file: PnP.PowerShell.dll-Help.xml
Module Name: PnP.PowerShell
online version: https://docs.microsoft.com/powershell/module/sharepoint-pnp/get-pnpfile
schema: 2.0.0
title: Get-PnPFile
---

# Get-PnPFile

## SYNOPSIS
Downloads a file.

## SYNTAX

### Return as file object (Default)
```
Get-PnPFile [-Url] <String> [-AsFileObject] [-Web <WebPipeBind>] [-Connection <PnPConnection>]
 [<CommonParameters>]
```

### Return as list item
```
Get-PnPFile [-Url] <String> [-AsListItem] [-ThrowExceptionIfFileNotFound] [-Web <WebPipeBind>]
 [-Connection <PnPConnection>] [<CommonParameters>]
```

### Save to local path
```
Get-PnPFile [-Url] <String> [-Path <String>] [-Filename <String>] [-AsFile] [-Force] [-Web <WebPipeBind>]
 [-Connection <PnPConnection>] [<CommonParameters>]
```

### Return as string
```
Get-PnPFile [-Url] <String> [-AsString] [-Web <WebPipeBind>] [-Connection <PnPConnection>] [<CommonParameters>]
```

## DESCRIPTION

## EXAMPLES

### EXAMPLE 1
```powershell
Get-PnPFile -Url /sites/project/_catalogs/themes/15/company.spcolor
```

Retrieves the file and downloads it to the current folder

### EXAMPLE 2
```powershell
Get-PnPFile -Url /sites/project/_catalogs/themes/15/company.spcolor -Path c:\temp -FileName company.spcolor -AsFile
```

Retrieves the file and downloads it to c:\temp\company.spcolor

### EXAMPLE 3
```powershell
Get-PnPFile -Url /sites/project/_catalogs/themes/15/company.spcolor -AsString
```

Retrieves the file and outputs its contents to the console

### EXAMPLE 4
```powershell
Get-PnPFile -Url /sites/project/_catalogs/themes/15/company.spcolor -AsFile
```

Retrieves the file and returns it as a File object

### EXAMPLE 5
```powershell
Get-PnPFile -Url /sites/project/_catalogs/themes/15/company.spcolor -AsListItem
```

Retrieves the file and returns it as a ListItem object

### EXAMPLE 6
```powershell
Get-PnPFile -Url _catalogs/themes/15/company.spcolor -Path c:\temp -FileName company.spcolor -AsFile
```

Retrieves the file by site relative URL and downloads it to c:\temp\company.spcolor

## PARAMETERS

### -AsFile

```yaml
Type: SwitchParameter
Parameter Sets: Save to local path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsFileObject
Retrieve the file contents as a file object.

```yaml
Type: SwitchParameter
Parameter Sets: Return as file object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsListItem
Returns the file as a listitem showing all its properties

```yaml
Type: SwitchParameter
Parameter Sets: Return as list item
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsString
Retrieve the file contents as a string

```yaml
Type: SwitchParameter
Parameter Sets: Return as string
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Connection
Optional connection to be used by the cmdlet. Retrieve the value for this parameter by either specifying -ReturnConnection on Connect-PnPOnline or by executing Get-PnPConnection.

```yaml
Type: PnPConnection
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filename
Name for the local file

```yaml
Type: String
Parameter Sets: Save to local path
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Overwrites the file if it exists.

```yaml
Type: SwitchParameter
Parameter Sets: Save to local path
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Local path where the file should be saved

```yaml
Type: String
Parameter Sets: Save to local path
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThrowExceptionIfFileNotFound
If provided in combination with -AsListItem, a System.ArgumentException will be thrown if the file specified in the -Url argument does not exist. Otherwise it will return nothing instead.

```yaml
Type: SwitchParameter
Parameter Sets: Return as list item
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Url
The URL (server or site relative) to the file

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServerRelativeUrl, SiteRelativeUrl

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Web
This parameter allows you to optionally apply the cmdlet action to a subweb within the current web. In most situations this parameter is not required and you can connect to the subweb using Connect-PnPOnline instead. Specify the GUID, server relative url (i.e. /sites/team1) or web instance of the web to apply the command to. Omit this parameter to use the current web.

```yaml
Type: WebPipeBind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.SharePoint.Client.File

## NOTES

## RELATED LINKS

[SharePoint Developer Patterns and Practices](https://aka.ms/sppnp)