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

> [!Note]
> Trust scores and vetting requirements are determined by The Campaign Registry (TCR) and participating carriers. Brand vetting is **required as per TCR** in the following cases:
> To achieve higher trust scores for better message throughput and delivery rates.
> Brand vetting for 10DLC (10-Digit Long Code) messaging is typically required for companies outside the Russell 3000 list.

To receive approval with The Campaign Registry, Teams administrators use the Teams Admin Center to pass their company’s Brand and Campaign information to The Campaign Registry.

Brands and Campaigns are reviewed by The Campaign Registry, which helps ensure SMS messaging integrity, compliance, and accountability with industry standards.

Through an approved Brand and Campaign, Teams administrators can then SMS-enable eligible Microsoft Calling Plan numbers.

Registration and SMS-enabling Teams Calling Plan numbers can be summarized in the following diagram:

:::image type="content" source="media/sms-tcr-registration-small.png" alt-text="Overview of the SMS enablement process for Teams Calling Plan numbers." lightbox="media/sms-tcr-registration-large.png":::

**You must receive approval for your Brand and Campaign configuration before any number can SMS enabled. Mobile operators will not accept SMS traffic from brands/campaigns that don't go through TCR registration, and Teams phone numbers can’t be SMS-enabled until the brand and campaign are approved.**

The Brand and Campaign approval requirement applies to businesses that do mass texting or marketing, as well as businesses that send individual messages, **even if it isn't for marketing purposes**.

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

## Regions

SMS is currently available for users in the following countries and regions:

- USA and Puerto Rico
- Canada

US, PR, and CA users can send SMS messages to numbers that are able to receive SMS and are regionally assigned to US, PR, or Canada recipients.

Teams users sending or receiving SMS messages outside of US, PR, or Canada isn't supported.

Check the [Microsoft 365 roadmap](https://www.microsoft.com/microsoft-365/roadmap) for developments.

## Licensing

In addition to registering the company Brand and Campaign for access to the 10DLC network, your users must be licensed with the following licenses:

- Teams
- Teams Phone
- Microsoft Teams Calling Plan

Inbound and outbound SMS messaging support is included in Microsoft Teams Calling Plans, for supported countries and regions.

### Message and message-segments

Accounting for a SMS messages is calculated by the maximum size of a single SMS message. The size of a single SMS message segment is 140 bytes or 160 GSM 7-bit-encoded, standard text characters.

When a sent SMS message exceeds the character limit, it is split into multiple segments. These segments are sent individually and reassembled by the recipient's device to form the complete message. Each message segment accounts for one Teams SMS message.

For example, if a Teams user sends a message that is 240 characters, requiring two message segments, the usage indicates a cost equivalent to two SMS messages in your billing.

The number of SMS message segments per Calling Plan license depends on the Microsoft Calling Plan assigned and can be determined in the following table:

|Teams Calling Plan | Supports SMS capability |Included SMS (threshold before paying overage) |
|:-----|:-----|:-----|
|PAYG (Pay-as-you-go) |Yes |0 |
|Domestic 120 |Yes |100 |
|Domestic |Yes |200 |
|Domestic + International |Yes | 200 |
|Teams Phone + Calling Plan Bundle |Yes |Phone + Domestic = 200 (if purchased as Calling Plan bundle) / Phone + PAYG = 0 (if purchased as PAYG bundle) |

The number of alloted messages in a Calling Plan accounts for a total of inbound messages received plus outbound messages sent.

As with calling minutes, the number of SMS messages allocated per licensed user are pooled at the tenant level. Overage charges don't apply until the resources pooled across all users’ plans in the tenant are consumed within the billing period.

## Usage and Billing

For Domestic Calling Plan licenses, allotted SMS messages are pooled for all SMS-enabled-users in the tenant, and there's support for overages.

For pay-as-you-go Calling Plan licenses, SMS messages are billed per use.

SMS usage in all Calling Plans accounts for sent and received messages.

All users within the same tenant in the US, PR, and CA with the same Calling Plan share a common pool of SMS messages.

For example, if 100 users in the United States and Canada or Puerto Rico have a Domestic Calling Plan, each is allocated 200 SMS, creating a shared pool of 20,000 SMS. Any inbound or outbound messages exceeding this pool are billed per-message. Pooling applies only to identical Calling Plans.

### Rate limiting

To ensure Microsoft's high quality of service consistent with provided SLAs, rate limits are applied to the number of messages that can be sent from a number. The rate limits depend on several factors, including:

- The tier of your Brand
- The 10DLC operator that is sending the SMS on your user's behalf
- The use case of the Campaign
 
When approving a Campaign, a daily cap for SMS messages is established. If your users are reaching this cap and being blocked by the rate limit, and their high volume of SMS messaging is warranted, you can apply for a rate limit increase by contacting [Microsoft's Telephone Number Services - Service Desk](contact-tns-service-desk.md).

### Usage fees

The price of a SMS message is accrued per-message segment. The per-message segment charge is based on the region of the message.

|Country/Region |Send Message |Receive Message |
|:-----|:-----|:-----|
|United States and Puerto Rico |$0.0075 USD |$0.0075 USD |
|Canada |$0.1028 CAD |$0.01028 CAD |

### Carrier fees

US and CA 10DLC operators apply a surcharge for processing SMS messages sent to and/or received by users on their network. For outbound messages, the surcharge is determined by the carrier of the recipient's number. For inbound messages, it is determined by the carrier of the sender's number.

For per-message segment pricing related to SMS usage, including currency conversions, see the following link: [SMS Pricing link](https://go.microsoft.com/fwlink/?linkid=2303326).

This surcharge is a per-message-segment fee that may vary over time. If the surcharge rates are expected to change, the SMS pricing table is updated 30 days before the implementation of any price changes.

### Billing and reporting

Detailed SMS usage on a per-message basis can be analyzed in the Teams Admin Center, under Analytics & reports.

Costs incurred for usage can be monitored and managed depending on the type of billing account that is used for invoicing. An example of billing account types and respective cost management methods can be reviewed in the following table:

|Billing account type |Cost management method |
|:-----|:-----|
|Microsoft Online Subscription Agreements, Enterprise Agreements, Legacy Direct, and Legacy Cloud Solution Partner (CSP) |Prepaid Communication Credits in the M365 admin center |
|Microsoft Customer Agreement via Direct or Enterprise |Postpaid Cost Management in the M365 admin center |
|Microsoft Customer Agreement via Cloud Solution Partner |Postpaid usage charges managed with partner |

For funding and analyzing costs related to prepaid or postpaid models, see the article [Microsoft Calling Plan overview](calling-plan-overview.md) and [Communication Credits](what-are-communications-credits.md).

## Considerations

One brand and one campaign are allowed per tenant.

By default, a campaign supports enabling up to 49 Microsoft Calling Plan numbers to be SMS-enabled. If more than 49 numbers need to be enabled for SMS, refer to note in [Step 2: Create campaign](sms-setup-campaign.md).

Once a number is SMS-enabled and assigned to a user, the user can begin sending and receiving messages. There is no policy governance to limit the number of messages sent to or received by the user.

Teams Calling Plans support sending SMS where the sender type is a 10 digit long code (1-234-123-1234). Teams Calling Plans do not currently support toll-free numbers (1-8XX), short codes (12345), or alphanumeric sender ID (CONTOSO).

Further prerequisites and next steps can be found in the following article: [Step 1: Create a brand](sms-setup-brand.md)

Support for **end users** can be found in the following article: [SMS support for Teams end users](https://support.microsoft.com/topic/a7d163cb-3562-4f4a-b1c1-81c722c1a0f1).

## Related topics

[Microsoft Calling Plan Overview](calling-plan-overview.md)

[Getting numbers with Microsoft Calling Plan](manage-phone-numbers-landing-page.md)

[Step 1: Create a brand](sms-setup-brand.md)
