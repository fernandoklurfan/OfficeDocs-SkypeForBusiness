---
title: Enabling and managing SMS operations in Teams Admin Center
author: sfrancis206
ms.author: scottfrancis
manager: pamgreen
ms.reviewer: nijait
ms.date: 01/06/2025
ms.topic: article
ms.tgt.pltfrm: cloud
ms.service: msteams
ms.collection:
  - M365-voice
  - m365initiative-voice
  - Tier1
search.appverid: MET150
audience: Admin
appliesto:
  - Microsoft Teams
ms.localizationpriority: medium
f1.keywords:
  - CSH
ms.custom:
  - Reporting
description: Enabling SMS usage and managing SMS operations in Teams Admin Center
---

# Enabling and managing SMS operations in Teams Admin Center

This article is for IT administrators and IT professionals who are administering the Short Message Service (SMS) usage in Microsoft’s Teams Admin Center (TAC).

## Prerequisites

### Brand and Campaign

To ensure successful enablement of SMS for a Teams Calling Plan phone number, confirm service enablement is configured, as described in the articles [Step 1: Create brand](sms-setup-brand.md) and [Step 2: Create campaign](sms-setup-campaign.md).

### Licensing

To proceed with enabling Teams users with SMS capabilities, the following must be provisioned:

- Users must be licensed with Teams, Teams Phone, and a Microsoft Teams Calling Plan. For more information, see [Licensing](sms-overview.md#licensing).
  
### Billing mechanism

A tenant **billing mechanism** *should* be in place for SMS consumption overages and *must* be in place for Pay-as-you-go Calling Plans.

- Funding for usage overages is supported either with prepaid Communication Credits using a Microsoft Online Subscription Agreement (MOSA) or with postpaid invoicing using a Microsoft Customer Agreement (MCA). For more information, see the article [Microsoft Calling Plan Overview](calling-plan-overview.md).

#### Permissions

Administrators must have one of the following Roles Based Access Control (RBAC) roles assigned:

- Teams Administrator
- Teams Communications Administrator
- Teams Telephony Administrator, or
- Global Admin

## Enabling SMS for a user

The first step in enabling SMS for a user is to SMS-enable the user's phone number. 

In Teams Admin Center (TAC), navigate to the left side rail, select ***Voice*** > ***Phone numbers*** > ***Numbers***, and then find and select the number for the user. In the contextual menu just above the list of phone numbers, select ***Enable SMS***

If the number isn't already assigned to a user, assign a user with the number. For more information on number management, see [Manage phone numbers for users](assign-change-or-remove-a-phone-number-for-a-user.md)

## Disabling SMS for a user

To disable a user, in Teams Admin Center (TAC), navigate to the left side rail, select ***Voice*** > ***Phone numbers*** > ***Numbers***, and then find and select the number for the user. In the contextual menu just above the list of phone numbers, select ***Disable SMS***

## Confirming usage

To confirm SMS usage, in Teams Admin Center, navigate to the left side rail, select **Reports & analytics** > **Usage reports** > **PSTN and SMS Usage**, choose a date range, and select **Run report**.

For more information, see [Microsoft Teams PSTN Usage report](.\teams-analytics-and-reports\pstn-usage-report.md).

## Related topics

[SMS overview](sms-overview.md)

[Step 1: Create brand](sms-setup-brand.md)

[Step 2: Create campaign](sms-setup-campaign.md)
