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

Microsoft Teams supports sending and receiving Short Message Service (SMS) text messages within Teams Chat, for users in US, Puerto Rico, and Canada.

All SMS messaging to and from Teams is considered:

- Business messaging
- Non-consumer messaging
- Application-to-Person (A2P) messaging.

These references are used interchangeably. Most notably, SMS in Teams is *not* categorized as *consumer* SMS messaging.

PSTN (Public Switched Telephone Network) operators support A2P messaging through a specialized network, designated as the 10DLC (10 Digit Long Code) network. Before an entity can transmit A2P SMS messages on the 10DLC network, the 10DLC operators must approve validity of a company and the company’s intent for accessing the network.

The shared, independent, approving authority, used by 10DLC network operators, is [The Campaign Registry](https://www.campaignregistry.com/about/). Microsoft is required to facilitate a customer’s registration with The Campaign Registry before Microsoft Calling Plan numbers can be enabled for SMS.

Registration with The Campaign Registry involves the following two parts:

1. A **Brand**: The identification and validation of your company
2. A **Campaign**: The purpose and context of your SMS operation

To receive approval with The Campaign Registry, Teams administrators use the Teams Admin Center to pass their company’s Brand and Campaign information to The Campaign Registry.

Brands and Campaigns are reviewed by The Campaign Registry, which helps ensure SMS messaging integrity, compliance, and accountability with industry standards.

Through an approved Brand and Campaign, Teams administrators can then SMS-enable eligible Microsoft Calling Plan numbers.

**You must receive approval for your Brand and Campaign configuration before any number can SMS enabled. Mobile operators will not accept SMS traffic from brands/campaigns that don't go through TCR registration, and Teams phone numbers can’t be SMS-enabled until the brand and campaign are approved.**

> [!NOTE]
> The Brand and Campaign approval requirement applies to businesses that do mass texting or marketing, as well as businesses that send individual messages, **even if it isn't for marketing purposes**.

When you apply for Brand approval, legally identifiable information about your company must be submitted, including things such as the following:

- Business ID
- Legal address
- Stock Symbol
- Website

More details can be found in [Step 1: Create a brand](sms-setup-brand.md)

When you apply for Campaign approval, resources about your company's campaign operation must be submitted, including things such as the following:

- SMS Use cases
- Message flow actions (describing opt-in and opt-out words)
- A2P SMS privacy statement
- A2P SMS Terms and conditions

More details can be found in [Step 2: Create campaign](sms-setup-campaign.md)

## Licensing

SMS licensing for users follows the same licensing model as Microsoft Teams Calling Plans. Sent and received messages are included in the Calling Plans.

In addition to registering the company Brand and Campaign for access to the 10DLC network, your users must be licensed with Teams, Teams Phone, and a Microsoft Teams Calling Plan.

The number of SMS messages per Calling Plan license depends on the Microsoft Calling Plan assigned and can be determined in the following table:

|Teams Calling Plan | Supports SMS capability |Included SMS (threshold before paying overage) |
|:-----|:-----|:-----|
|PAYG (Pay-as-you-go) |Yes |0 |
|Domestic 120 |Yes |100 |
|Domestic |Yes |200 |
|Domestic + International |Yes | 200 |
|Teams Phone + Calling Plan Bundle |Yes |Phone + Domestic = 200 (if purchased as Calling Plan bundle) / Phone + PAYG = 0 (if purchased as PAYG bundle) |

Calling minutes and SMS messages allocated per licensed user are pooled at the tenant level. Overage charges don't apply until the resources pooled across all users’ plans in the tenant are consumed within the billing period.

## Regions

SMS is currently available for users in the following countries and regions:

- USA and Puerto Rico
- Canada

US, PR, and CA users can send SMS messages to numbers that are able to receive SMS and are regionally assigned to US, PR, or Canada recipients.

Teams users sending SMS to numbers outside of US, PR, or Canada isn't supported, but Teams user can receive SMS messages from any country or region.

Check the [Microsoft 365 roadmap](https://www.microsoft.com/microsoft-365/roadmap) for developments.

## Usage

For domestic Calling Plan licenses, similar to Calling Plan minutes, allotted SMS messages are pooled for all SMS-enabled-users in the tenant, and there's support for overages.

For pay-as-you-go Calling Plan licenses, SMS messages are billed per use.

SMS usage in all Calling Plans includes sent and received messages.

All users within the same tenant in the US, PR, and CA with the same Calling Plan share a common pool of SMS messages. For example, if 100 users in the United States and Canada or Puerto Rico have a Domestic Calling Plan, each is allocated 200 SMS, creating a shared pool of 20,000 SMS. Any inbound or outbound messages exceeding this pool are billed per-message. Pooling applies only to identical Calling Plans.

Once a number is SMS-enabled and assigned to a user, the user can begin sending and receiving messages. There is no policy governance to limit the number of messages sent to or received by the user.

Detailed SMS usage on a per-message basis can be analyzed in the Teams Admin Center, under Analytics & reports.

Costs incurred for usage can be monitored depending on the type of billing account that is used for invoicing. An example of billing account types and respective cost management methods can be reviewed in the following table:

|Billing account type |Cost management method |
|:-----|:-----|
|Microsoft Online Subscription Agreements, Enterprise Agreements, Legacy Direct, and Legacy Cloud Solution Partner (CSP) |Prepaid Communication Credits in the M365 admin center |
|Microsoft Customer Agreement via Direct or Enterprise |Postpaid Cost Management in the M365 admin center |
|Microsoft Customer Agreement via Cloud Solution Partner |Postpaid usage charges managed with partner |

For funding and analyzing costs related to prepaid or postpaid models, see the article [Microsoft Calling Plan overview](calling-plan-overview.md) and [Communication Credits](what-are-communications-credits.md).

For per-message pricing related to SMS usage, see [SMS Pricing link](https://go.microsoft.com/fwlink/?linkid=2303326).

## Considerations

One brand and one campaign are allowed per tenant.

By default, a campaign supports enabling up to 49 Microsoft Calling Plan numbers to be SMS-enabled. If more than 49 numbers need to be enabled for SMS, refer to note in [Step 2: Create campaign](sms-setup-campaign.md).

Further prerequisites and next steps can be found in the following article: [Step 1: Create a brand](sms-setup-brand.md)

Support for end users wanting to send SMS messages in Teams can be found in the following article: [SMS support for Teams end users](https://support.microsoft.com/en-us/topic/a7d163cb-3562-4f4a-b1c1-81c722c1a0f1?preview=true).

## Related topics

[Microsoft Calling Plan Overview](calling-plan-overview.md)

[Getting numbers with Microsoft Calling Plan](manage-phone-numbers-landing-page.md)

[Step 1: Create a brand](sms-setup-brand.md)
