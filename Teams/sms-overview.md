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

These references are used interchangeably.

When you SMS-enable a Calling Plan phone number in Teams Admin Center, on your behalf Microsoft registers the number to an ecosystem of mobile operators who support the industry’s 10DLC (10-digit long code) network.

Before a phone number can be sanctioned for use on the 10DLC network for A2P messaging, required information must be supplied to and reviewed by an independent reputation authority for approval. Microsoft uses [The Campaign Registry](https://www.campaignregistry.com/about/) for this purpose.

The Teams Admin Center facilitates collection of required information to supply to The Campaign Registry (TCR) by allowing Teams Administrators to input information about their company (their “Brand”) and about the intention of their SMS usage (their “Campaign”).

Your non-consumer, business text messaging Brands and Campaigns are reviewed by TCR, which helps ensure business SMS messaging compliance and accountability with industry standards.

Through the approved Brand and Campaign registration, your 10DLC numbers are then recognized by mobile network operators as compliant for application-to-person messaging.

It is necessary to receive approval for your Brand and Campaign configuration before any number can be registered for use in the 10DLC ecosystem, or SMS-enabled. This requirement applies to businesses that do mass texting or marketing, as well as businesses that send individual messages, **even if it is not for marketing purposes**.

The Campaign Registry approval and 10DLC registration involves a TAC setup process that requires three key steps:

- Brand verification
- Campaign registration
- SMS number activation

You must achieve successful 10DLC registration by setting up your Brand and Campaign before you can enable any user's number with SMS capability.

## Architecture

<<<find / use diagram>>>

## Considerations

You are allowed one brand and campaign per tenant.

SMS is available for Teams users with a Microsoft Calling Plan license and phone number assigned, and is currently available for users in the following countries and regions:

- USA and Puerto Rico
- Canada

SMS for Teams users in other countries and regions, where Microsoft Calling Plans are available, is in development. Check the [Microsoft 365 roadmap](https://www.microsoft.com/microsoft-365/roadmap) for developments.

USA and Puerto Rico users can send SMS messages to recipients in the USA, Puerto Rico, and Canada.

Canada users can send SMS messages to recipients in Canada, the USA and Puerto Rico.

For domestic and domestic plus international Calling Plan licenses, 200 SMS messages are allowed per month. Similar to Calling Plan minutes, SMS message entitlements are pooled for all SMS-enabled-users in the tenant.

For pay-as-you-go Calling Plan licenses, SMS messages are incrementally billed per message.

Billing for overages and pay-as-you-go follows either the Pre-paid or post-paid models, outlined in the article [Microsoft Calling Plan overview](calling-plan-overview.md)

Further prerequisites and next steps can be found in the following article: [Setting up SMS in TAC](sms-setup-brand-and-campaign.md)

## Related topics

[Microsoft Calling Plan Overview](calling-plan-overview.md)

[Getting numbers with Microsoft Calling Plan](manage-phone-numbers-landing-page.md)

[Setting up SMS in TAC](sms-setup-brand-and-campaign.md)
