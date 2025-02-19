---
title: "Manage phone numbers for users"
author: sfrancis206
ms.author: scottfrancis
manager: pamgreen
ms.reviewer: julienp, roykuntz, jastark
ms.date: 02/14/2024
ms.topic: article
ms.assetid: 91089761-cb87-4119-885b-3713840dd9f7
ms.tgt.pltfrm: cloud
audience: admin
ms.service: msteams
search.appverid: MET150
ms.collection: 
- M365-voice
- m365initiative-voice
- Tier1
appliesto:
  - Microsoft Teams
ms.localizationpriority: medium
f1.keywords:
- CSH
ms.custom:
  - Calling Plans
description: "Learn how to assign, change, or remove a work phone number for your Teams users so outside businesses and clients can call in."
---

# Manage phone numbers for users

This article provides guidance on assigning, changing, or removing a number for a user.

## Prerequisites

Before you can assign a number to a user you must get numbers for your organization. For more information, see [Manage telephone numbers for your organization](manage-phone-numbers-landing-page.md).

When assigning a phone number to a user, make sure the phone number and the usage location of the user are of the same country/region.

You must have one of the following roles to assign, modify, or remove a number for a user:

- Teams Administrator
- Teams Communications Administrator
- Teams Telephony Administrator

If the user is to be assigned with a Teams Calling Plan number, the user must also have a Teams Calling Plan license.

> [!NOTE]
> Teams Calling Plan licenses are assigned in the **Microsoft 365 admin center**. To see whether a user has a license assigned in the **Teams admin center**, navigate to **Users** > **Manage users**. In the list, find the column heading **Calling Plan**. If a license is assigned, the license will be indicated in this view.

> [!NOTE]
> This note applies to customers who have a hybrid deployment with an on-premises Active Directory. If you want to assign a Calling Plan or Operator Connect phone number to a user or resource account, you must ensure that any phone number stored in the msRTCSIP-Line attribute on the user or resource account object in the on-premises Active Directory has been removed, and the change has been synchronized to Microsoft 365.

## Use Teams Admin Center to assign a phone number to a user

This method applies to all PSTN Connectivity type numbers. However, using this method for Direct Routing numbers only works if you opted to upload your Direct Routing numbers to Teams. For more information, see [Upload Direct Routing numbers to your tenant](direct-routing-enable-users.md#upload-direct-routing-numbers-to-your-tenant).

1. Navigate to the Microsoft Teams admin center.

2. In the left navigation, click **Voice** > **Phone numbers**.

3. On the **Phone numbers** page, select an unassigned number in the list, and then click **Edit**.

4. In the **Edit** pane, under **Assigned to**, search for the user by display name or user name, and then click **Assign**.

5. To assign or change the associated emergency location, under **Emergency location**, search for and then select the location.

> [!NOTE]
> If you are assigning numbers to Operator Connect or Operator Connect Mobile users, you may or may not be able to assign or change the associated emergency location. This functionality will depend on your Operator. Contact your Operator for more information.

6. Depending on whether you want to send an email to the user with their phone number information, turn off or turn on **Email user with telephone number information**. By default, this is on.

7. Select **Save**.

### Use PowerShell to assign a phone number to a user

To assign numbers by using PowerShell, use the [Set-CsPhoneNumberAssignment](/powershell/module/teams/set-csphonenumberassignment) cmdlet as follows:

For Calling Plan numbers:

```PowerShell
Set-CsPhoneNumberAssignment -Identity <user> -PhoneNumber <phone number> -PhoneNumberType CallingPlan
```

For Operator Connect numbers:

```PowerShell
Set-CsPhoneNumberAssignment -Identity <user> -PhoneNumber <phone number> -PhoneNumberType OperatorConnect
```

For Teams Phone Mobile numbers:

```PowerShell
Set-CsPhoneNumberAssignment -Identity <user> -PhoneNumber <phone number> -PhoneNumberType OperatorConnect
```

For Direct Routing numbers:

```PowerShell
Set-CsPhoneNumberAssignment -Identity <user> -PhoneNumber <phone number> -PhoneNumberType DirectRouting
```

For example:

```PowerShell
Set-CsPhoneNumberAssignment -Identity john@contoso.com -PhoneNumber "+14255550101" -PhoneNumberType CallingPlan
Set-CsPhoneNumberAssignment -Identity jack@contoso.com -PhoneNumber "+14255550102" -PhoneNumberType OperatorConnect
```

> [!NOTE]
> Because of the latency between Microsoft 365 and Teams, it can take up to 24 hours for users to be enabled. If the phone number isn't assigned correctly after 24 hours, see [Phone Number Service Center](https://pstnsd.powerappsportals.com/).

> [!NOTE]
> When you assign a phone number, the user's Entra ID object attribute **EnterpriseVoiceEnabled** is automatically set to True.

## Use Teams admin center to change a phone number for a user

To change a phone number for a user by using the Teams admin center:

1. In the left navigation, click **Users** > **Manage users**, locate and select the user you want. In the user's profile, select the tab **Account**, and then under **Assigned phone number**, make a note of the phone number that's assigned to the user and select **Edit**.

2. In the right side rail, from the **Phone number type** drop down menu, select the PSTN connectivity type that is supplying the new telephone number.

3. From the **Assigned phone number** drop down menu, find and select the new number.

4. Select the **Emergency location** to associate with the phone number and user.

> [!NOTE]
> If you are changing numbers for Operator Connect or Teams Phone Mobile users, you may or may not be able to assign or change the associated emergency location. This functionality will depend on your Operator. Contact your Operator for more information.

5. Depending on whether you want to send an email to the user with their new phone number information, turn off or turn on **Email user with telephone number information**. By default, this is on.

6. Select **Save**.

### Use PowerShell to change a phone number for a user

For a PowerShell example, see [Set-CsPhoneNumberAssignment](/powershell/module/teams/set-csphonenumberassignment).

## Use Teams admin center to remove a phone number from a user

To remove a phone number by using the Teams admin center:

1. In the left navigation, click **Users** > **Manage users**, locate and select the user you want. In the user's profile, select the tab **Account**, and then under **Assigned phone number**, make a note of the phone number that's assigned to the user and select **Edit**.

2. In the right side rail, from the **Asssigned phone number** drop down menu, select **None**.

3. Select **Apply**.

### Use PowerShell to remove a phone number for a user

For a PowerShell example, see [Remove-CsPhoneNumberAssignment](/powershell/module/teams/remove-csphonenumberassignment).

For more information about assigning, changing, or removing a phone number from a user in a Direct Routing scenario, see [Enable users for Direct Routing, voice, and voicemail](./direct-routing-enable-users.md).

## Related topics

[Manage phone numbers for your organization](/microsoftteams/manage-phone-numbers-for-your-organization)

[Manage the usage of a phone number](/microsoftteams/manage-the-usage-of-a-phone-number)

[Set-CsPhoneNumberAssignment](/powershell/module/teams/set-csphonenumberassignment)

[Plan your Teams Voice solution](/microsoftteams/cloud-voice-landing-page)
