---
external help file: Microsoft.Exchange.TransportMailflow-Help.xml
online version: https://docs.microsoft.com/powershell/module/exchange/set-autosensitivitylabelpolicy
applicable: Security & Compliance Center
title: Set-AutoSensitivityLabelPolicy
schema: 2.0.0
author: chrisda
ms.author: chrisda
ms.reviewer:
---

# Set-AutoSensitivityLabelPolicy

## SYNOPSIS
This cmdlet is available only in Security & Compliance Center PowerShell. For more information, see [Security & Compliance Center PowerShell](https://docs.microsoft.com/powershell/exchange/scc-powershell).

Use the Set-AutoSensitivityLabelPolicy cmdlet to modify auto-labeling policies in your organization.

For information about the parameter sets in the Syntax section below, see [Exchange cmdlet syntax](https://docs.microsoft.com/powershell/exchange/exchange-cmdlet-syntax).

## SYNTAX

### Identity
```
Set-AutoSensitivityLabelPolicy [-Identity] <PolicyIdParameter>
 [-AddExchangeLocation <MultiValuedProperty>]
 [-AddOneDriveLocation <MultiValuedProperty>]
 [-AddOneDriveLocationException <MultiValuedProperty>]
 [-AddSharePointLocation <MultiValuedProperty>]
 [-AddSharePointLocationException <MultiValuedProperty>]
 [-ApplySensitivityLabel <String>]
 [-Comment <String>]
 [-Confirm]
 [-Enabled <Boolean>]
 [-ExchangeSender <SmtpAddress[]>]
 [-ExchangeSenderException <SmtpAddress[]>]
 [-ExchangeSenderMemberOf <SmtpAddress[]>]
 [-ExchangeSenderMemberOfException <SmtpAddress[]>]
 [-Force]
 [-Mode <PolicyMode>]
 [-Priority <System.Int32>]
 [-RemoveExchangeLocation <MultiValuedProperty>]
 [-RemoveOneDriveLocation <MultiValuedProperty>]
 [-RemoveOneDriveLocationException <MultiValuedProperty>]
 [-RemoveSharePointLocation <MultiValuedProperty>]
 [-RemoveSharePointLocationException <MultiValuedProperty>]
 [-StartSimulation <Boolean>]
 [-WhatIf]
 [<CommonParameters>]
```

### TeamLocation
```
Set-AutoSensitivityLabelPolicy [-Identity] <PolicyIdParameter>
 [-Comment <String>]
 [-Confirm]
 [-Enabled <Boolean>]
 [-Force]
 [-Mode <PolicyMode>]
 [-WhatIf]
 [<CommonParameters>]
```

### RetryDistributionParameterSet
```
Set-AutoSensitivityLabelPolicy [-Identity] <PolicyIdParameter>
 [-Confirm]
 [-Mode <PolicyMode>]
 [-RetryDistribution]
 [-WhatIf]
 [<CommonParameters>]
```

## DESCRIPTION
To use this cmdlet in Security & Compliance Center PowerShell, you need to be assigned permissions. For more information, see [Permissions in the Microsoft 365 compliance center](https://docs.microsoft.com/microsoft-365/compliance/microsoft-365-compliance-center-permissions).

## EXAMPLES

### Example 1
```powershell
Set-AutoSensitivityLabelPolicy -Identity "Main PII" -AddSharePointLocation "https://my.url1","https://my.url2" -AddOneDriveLocation "https://my.url3","https://my.url4"
```

This example adds the specified URLs to the SharePoint Online and OneDrive for Business locations for the autolabeling policy named Main PII without affecting the existing URL values.

## PARAMETERS

### -Identity
The Identity parameter specifies the auto-labeling policy that you want to modify. You can use any value that uniquely identifies the policy. For example:

- Name
- Distinguished name (DN)
- GUID

```yaml
Type: PolicyIdParameter
Parameter Sets: (All)
Aliases:
Applicable: Security & Compliance Center

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -AddExchangeLocation
This AddExchangeLocation parameter specifies new Exchange locations to be added to the policy without affecting the existing ones.

```yaml
Type: MultiValuedProperty
Parameter Sets: Identity
Aliases:
Applicable: Security & Compliance Center

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddOneDriveLocation
The AddOneDriveLocation parameter specifies the OneDrive for Business sites to add to the list of included sites when you aren't using the value All for the OneDriveLocation parameter. You identify the site by its URL value.

To enter multiple values, use the following syntax: <value1>,<value2>,...<valueX>. If the values contain spaces or otherwise require quotation marks, use the following syntax: "<value1>","<value2>",..."<valueX>".

```yaml
Type: MultiValuedProperty
Parameter Sets: Identity
Aliases:
Applicable: Security & Compliance Center

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddOneDriveLocationException
The AddOneDriveLocationException parameter specifies the OneDrive for Business sites to add to the list of excluded sites when you use the value All for the OneDriveLocation parameter. You identify the site by its URL value.

To enter multiple values, use the following syntax: <value1>,<value2>,...<valueX>. If the values contain spaces or otherwise require quotation marks, use the following syntax: "<value1>","<value2>",..."<valueX>".

```yaml
Type: MultiValuedProperty
Parameter Sets: Identity
Aliases:
Applicable: Security & Compliance Center

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddSharePointLocation
The AddSharePointLocation parameter specifies the SharePoint Online sites to add to the list of included sites when you aren't using the value All for the SharePointLocation parameter. You identify the site by its URL value.

SharePoint Online sites can't be added to the policy until they have been indexed.

To enter multiple values, use the following syntax: <value1>,<value2>,...<valueX>. If the values contain spaces or otherwise require quotation marks, use the following syntax: "<value1>","<value2>",..."<valueX>".

```yaml
Type: MultiValuedProperty
Parameter Sets: Identity
Aliases:
Applicable: Security & Compliance Center

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddSharePointLocationException
The AddSharePointLocationException parameter specifies the SharePoint Online sites to add to the list of excluded sites when you use the value All for the SharePointLocation parameter. You identify the site by its URL value.

To enter multiple values, use the following syntax: <value1>,<value2>,...<valueX>. If the values contain spaces or otherwise require quotation marks, use the following syntax: "<value1>","<value2>",..."<valueX>". }}

```yaml
Type: MultiValuedProperty
Parameter Sets: Identity
Aliases:
Applicable: Security & Compliance Center

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplySensitivityLabel
The ApplySensitivityLabel parameter selects which label to be used for the policy. This will override the previous label on the policy.

```yaml
Type: String
Parameter Sets: Identity
Aliases:
Applicable: Security & Compliance Center

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Comment
The Comment parameter specifies an optional comment. If you specify a value that contains spaces, enclose the value in quotation marks ("), for example: "This is an admin note".

```yaml
Type: String
Parameter Sets: Identity, TeamLocation
Aliases:
Applicable: Security & Compliance Center

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
The Confirm switch specifies whether to show or hide the confirmation prompt. How this switch affects the cmdlet depends on if the cmdlet requires confirmation before proceeding.

- Destructive cmdlets (for example, Remove-\* cmdlets) have a built-in pause that forces you to acknowledge the command before proceeding. For these cmdlets, you can skip the confirmation prompt by using this exact syntax: `-Confirm:$false`.
- Most other cmdlets (for example, New-\* and Set-\* cmdlets) don't have a built-in pause. For these cmdlets, specifying the Confirm switch without a value introduces a pause that forces you acknowledge the command before proceeding.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf
Applicable: Security & Compliance Center

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enabled
The Enabled parameter enables or disables the policy. Valid values are:

- $true: The policy is enabled. This is the default value.
- $false: The policy is disabled.

```yaml
Type: Boolean
Parameter Sets: Identity, TeamLocation
Aliases:
Applicable: Security & Compliance Center

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExchangeSender
The ExchangeSender parameter specifies the sender list in Exchange for which the policy should include.

```yaml
Type: SmtpAddress[]
Parameter Sets: Identity
Aliases:
Applicable: Security & Compliance Center

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExchangeSenderException
The ExchangeSenderException parameter specifies the sender list in Exchange for which the policy should exclude.

```yaml
Type: SmtpAddress[]
Parameter Sets: Identity
Aliases:
Applicable: Security & Compliance Center

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExchangeSenderMemberOf
The ExchangeSenderMemberOf parameter specifies the distribution groups, mail-enabled security groups, or dynamic distribution groups to include in the autolabeling policy. You identify the group by its email address.

To enter multiple values, use the following syntax: <value1>,<value2>,...<valueX>.

You can't use this parameter to specify Microsoft 365 Groups.

```yaml
Type: SmtpAddress[]
Parameter Sets: Identity
Aliases:
Applicable: Security & Compliance Center

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExchangeSenderMemberOfException
The ExchangeSenderMemberOf parameter specifies the distribution groups, mail-enabled security groups, or dynamic distribution groups to exclude from the autolabeling policy. You identify the group by its email address.

To enter multiple values, use the following syntax: <value1>,<value2>,...<valueX>.

You can't use this parameter to specify Microsoft 365 Groups.

```yaml
Type: SmtpAddress[]
Parameter Sets: Identity
Aliases:
Applicable: Security & Compliance Center

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
The Force switch hides warning or confirmation messages. You don't need to specify a value with this switch.

You can use this switch to run tasks programmatically where prompting for administrative input is inappropriate.

```yaml
Type: SwitchParameter
Parameter Sets: Identity, TeamLocation
Aliases:
Applicable: Security & Compliance Center

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Mode
The Mode parameter specifies the action and notification level of the autolabel policy. Valid values are:

- Enable: The policy is enabled for actions and notifications.
- Disable: The policy is disabled.
- TestWithNotifications: Not supported.
- TestWithoutNotifications: An audit mode where no actions are taken, and no notifications are sent (Test mode).

```yaml
Type: PolicyMode
Parameter Sets: (All)
Aliases:
Accepted values: Enable, TestWithNotifications, TestWithoutNotifications, Disable, PendingDeletion
Applicable: Security & Compliance Center

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priority
The Priority parameter specifies a priority value for the policy that determines the order of policy processing. A lower integer value indicates a higher priority, the value 0 is the highest priority, and policies can't have the same priority value.

Valid values and the default value for this parameter depend on the number of existing policies. For example, if there are 5 existing policies:

- Valid priority values for the existing 5 policies are from 0 through 4.
- Valid priority values for a new 6th policy are from 0 through 5.
- The default value for a new 6th policy is 5.

If you modify the priority value of a policy, the position of the policy in the list changes to match the priority value you specify. In other words, if you set the priority value of a policy to the same value as an existing policy, the priority value of the existing policy and all other lower priority policies after it is increased by 1.

```yaml
Type: System.Int32
Parameter Sets: Identity
Aliases:
Applicable: Security & Compliance Center

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveExchangeLocation
The RemoveExchangeLocation parameter removes locations on Exchange from the policy.

```yaml
Type: MultiValuedProperty
Parameter Sets: Identity
Aliases:
Applicable: Security & Compliance Center

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveOneDriveLocation
The RemoveOneDriveLocation parameter specifies the OneDrive for Business sites to remove from the list of included sites when you aren't using the value All for the OneDriveLocation parameter. You identify the site by its URL value.

To enter multiple values, use the following syntax: <value1>,<value2>,...<valueX>. If the values contain spaces or otherwise require quotation marks, use the following syntax: "<value1>","<value2>",..."<valueX>".

```yaml
Type: MultiValuedProperty
Parameter Sets: Identity
Aliases:
Applicable: Security & Compliance Center

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveOneDriveLocationException
This RemoveOneDriveLocationException parameter specifies the OneDrive for Business sites to remove from the list of excluded sites when you use the value All for the OneDriveLocation parameter. You identify the site by its URL value.

To enter multiple values, use the following syntax: <value1>,<value2>,...<valueX>. If the values contain spaces or otherwise require quotation marks, use the following syntax: "<value1>","<value2>",..."<valueX>".

```yaml
Type: MultiValuedProperty
Parameter Sets: Identity
Aliases:
Applicable: Security & Compliance Center

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveSharePointLocation
The RemoveSharePointLocation parameter specifies the SharePoint Online sites to remove from the list of included sites when you aren't using the value All for the SharePointLocation parameter. You identify the site by its URL value.

To enter multiple values, use the following syntax: <value1>,<value2>,...<valueX>. If the values contain spaces or otherwise require quotation marks, use the following syntax: "<value1>","<value2>",..."<valueX>".

```yaml
Type: MultiValuedProperty
Parameter Sets: Identity
Aliases:
Applicable: Security & Compliance Center

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveSharePointLocationException
The RemoveSharePointLocationException parameter specifies the SharePoint Online sites to remove from the list of excluded sites when you use the value All for the SharePointLocation parameter. You identify the site by its URL value.

To enter multiple values, use the following syntax: <value1>,<value2>,...<valueX>. If the values contain spaces or otherwise require quotation marks, use the following syntax: "<value1>","<value2>",..."<valueX>".

```yaml
Type: MultiValuedProperty
Parameter Sets: Identity
Aliases:
Applicable: Security & Compliance Center

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetryDistribution
The RetryDistribution switch redistributes the policy to all OneDrive for Business and SharePoint Online locations. You don't need to specify a value with this switch.

Locations whose initial distributions succeeded aren't included in the retry. Policy distribution errors are reported when you use this switch.

**Note**: Because the process of retrying distribution is a significant operation, run it only if necessary and for one policy at a time. It is not intended to be run every time you update a policy. If you run a script to update multiple policies, wait until the policy distribution is successful before running the command again for the next policy.

```yaml
Type: SwitchParameter
Parameter Sets: RetryDistributionParameterSet
Aliases:
Applicable: Security & Compliance Center

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartSimulation
Use the StartSimulation parameter to restart the simulation for updated results. Valid values are:

- $true: Restart the simulation for updated results.
- $false: This is the default value

```yaml
Type: Boolean
Parameter Sets: Identity
Aliases:
Applicable: Security & Compliance Center
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
The WhatIf switch doesn't work in Security & Compliance Center PowerShell.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi
Applicable: Security & Compliance Center

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

###  

## OUTPUTS

###  

## NOTES

## RELATED LINKS
