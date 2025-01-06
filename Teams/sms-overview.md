---
title: SMS in Teams
author: sfrancis205
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

Before you start, review prerequisite knowledge referenced in the following articles: [Setting up SMS in TAC](sms-setup-brand-and-campaign.md)

## Overview

Microsoft Teams supports sending and receiving Simple Messaging Service (SMS) text messages within Teams Chat.

All SMS messaging to and from Teams is considered:

- Business messaging
- Non-consumer messaging
- Application-to-Person (A2P) messaging.

These references are used interchangeably.

When Microsoft SMS-enables a Calling Plan phone number, they are registering the number to an ecosystem of mobile operators who support the industry’s 10DLC (10-digit long code) network.

Before a phone number can be sanctioned for use on the 10DLC network for A2P messaging, required information must be supplied to an independent reputation authority for approval. The Teams Admin Center facilitates this collection of information by allowing Teams Administrators to input information about the company (their “Brand”) and about the intention of the A2P messaging usage (the “Campaign”).

Your non-consumer, business text messaging brands and campaigns are reviewed by The Campaign Registry (TCR), which helps ensure business SMS messaging compliance and accountability with industry standards.

It is necessary to receive approval for at least one Brand and one Campaign before any number can be registered for use in the 10DLC ecosystem, or SMS-enabled. This requirement applies to businesses that do mass texting or marketing, as well as businesses that send individual messages, **even if it is not for marketing purposes**.

Submitting a Brand and a Campaign for registration requires a review and approval process.

Through the approved Brand and Campaign registration, your 10DLC numbers are then recognized by mobile network operators as compliant for application-to-person messaging.

The TCR registration and 10DLC classification includes a TAC provisioning process that requires three key steps:

- Brand verification
- Campaign registration
- SMS number activation

You must achieve successful TCR registration before you can enable any number with SMS capability.

You are allowed one brand and campaign per tenant.

> [!NOTE]
> <<<Clarify context with (why only) one brand and one campaign per tenant, here>>>

## Architecture


## Considerations


## Related topics

[Microsoft Calling Plan Overview](calling-plan-overview.md)

[Getting numbers with Microsoft Calling Plan](manage-phone-numbers-landing-page.md)

[Setting up SMS in TAC](sms-setup-brand-and-campaign.md)
