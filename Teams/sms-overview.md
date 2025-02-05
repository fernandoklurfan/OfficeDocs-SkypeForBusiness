---
title: SMS in Teams
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
description: Learn about SMS texting in Teams
---

# SMS texting in Teams with Microsoft Calling Plan numbers

This article is for IT administrators and IT professionals planning to enable Short Message Service (SMS) for their tenant in Microsoft’s Teams Admin Center (TAC).

## Overview

Microsoft Teams supports sending and receiving Simple Messaging Service (SMS) text messages within Teams Chat.

All SMS messaging to and from Teams is considered:

- Business messaging
- Non-consumer messaging
- Application-to-Person (A2P) messaging.

These references are used interchangeably. Most notably, SMS in Teams is *not* categorized as *consumer* SMS messaging.

PSTN (Public Switched Telephone Network) operators support A2P messaging through a specialized network, designated as the 10DLC (Ten Digit Long Code) network. Before an entity can transmit A2P SMS messages on the 10DLC network, the 10DLC operators must approve validity of a company and the company’s intent for accessing it.

The shared, independent, approving authority for 10DLC network operators is [The Campaign Registry](https://www.campaignregistry.com/about/). Microsoft is required to facilitate a customer’s registration with The Campaign Registry before Microsoft Calling Plan numbers can be enabled for SMS.

Registration with The Campaign Registry involves the following two parts:

1. A **Brand**: The identification and validation of your company
2. A **Campaign**: The purpose and context of your SMS operation

To receive approval with The Campaign Registry, Teams administrators use the Teams Admin Center to pass their company’s Brand and Campaign information to The Campaign Registry.

Brands and Campaigns are reviewed by The Campaign Registry, which helps ensure SMS messaging integrity, compliance, and accountability with industry standards.

Through an approved Brand and Campaign, Teams administrators can then SMS-enable desired Microsoft Calling Plan numbers.

You must receive approval for your Brand and Campaign configuration before any number can SMS enabled. Mobile operators will not accept SMS traffic from brands/campaigns that don't go through TCR registration, and Teams phone numbers can’t be SMS-enabled until the brand and campaign are approved.

> [!NOTE]
> The Brand and Campaign approval requirement applies to businesses that do mass texting or marketing, as well as businesses that send individual messages, **even if it is not for marketing purposes**.

When applying for Brand approval, legally identifiable information about the company must be submitted, including things such as the  Business ID, Legal address, Stock Symbol, and website. More details can be found in [Step 1: Create a brand](sms-setup-brand.md)

When applying for Campaign approval, resources about the campaign operation must be submitted, including use case, message flow actions, Brand privacy statement and terms and conditions.
More details can be found in [Step 2: Create campaign](sms-setup-campaign.md)

## Considerations

SMS is available for Teams users with a Microsoft Calling Plan license and phone number assigned, and is currently available for users in the following countries and regions:

- USA and Puerto Rico
- Canada

Check the [Microsoft 365 roadmap](https://www.microsoft.com/microsoft-365/roadmap) for developments.

USA and Puerto Rico users can send SMS messages to recipients in the USA, Puerto Rico, and Canada.

Canada users can send SMS messages to recipients in Canada, the USA and Puerto Rico.

One brand and one campaign are allowed per tenant.

For domestic and domestic plus international Calling Plan licenses, similar to Calling Plan minutes, SMS message entitlements are pooled for all SMS-enabled-users in the tenant.

For pay-as-you-go Calling Plan licenses, SMS messages are incrementally billed per message, including sent and received messages.

|Teams Calling Plan | Supports SMS capability |Included SMS (threshold before paying overage) |
|:-----|:-----|:-----|
|PAYG |Yes |0 |
|Domestic 120 |Yes |100|
|Domestic 240 (deprecated) |No | 0 |
|Domestic 3000 |Yes |200 |
|International Only |(has pre-req of Domestic Only) |0 |
|Domestic + International |Yes | 200 |
|Teams Phone + Calling Plan |Yes |Phone + Domestic = 200, Phone + PAYG = 0 |

Billing for overages and pay-as-you-go follows either the Pre-paid or post-paid models, outlined in the article [Microsoft Calling Plan overview](calling-plan-overview.md)

Further prerequisites and next steps can be found in the following article: [Step 1: Create a brand](sms-setup-brand.md)

## Related topics

[Microsoft Calling Plan Overview](calling-plan-overview.md)

[Getting numbers with Microsoft Calling Plan](manage-phone-numbers-landing-page.md)

[Step 1: Create a brand](sms-setup-brand.md)
