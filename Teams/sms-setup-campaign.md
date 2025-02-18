---
title: Setting up SMS Campaign in Teams Admin Center
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
description: How to setup a SMS Campaign in Teams Admin Center
---

# Setting up SMS Campaign in Teams Admin Center

This article is for IT administrators and IT professionals who are enabling Short Message Service (SMS) in Teams. It's an accompaniment when using Microsoft’s Teams Admin Center (TAC) to register their company's SMS campaign with The Campaign Registry (TCR).

## Prerequisites

Ensure fundamental understanding of the **purpose** for a Campaign, as described in the article, [Learn about SMS Texting in Teams](sms-overview.md)

Administrators must have one of the following **RBAC roles** assigned:

- Teams Administrator
- Teams Communications Administrator, or
- Teams Telephony Administrator

## Building a Campaign

After your brand is registered with The Campaign Registry and reflected in Teams admin center as "Approved", proceed with the campaign registration.

The 10DLC (10-digit long code) registration process involves verifying your organization's intent and ability to use the 10DLC network in compliance. To get your intent approved, you submit your "Campaign" details to The Campaign Registry (TCR) via the Teams admin center.

The Teams Admin Center allows you to provide the minimum details about your company's Campaign. If The Campaign Registry rejects your Campaign application, a support case will be opened automatically and Microsoft's Telephone Number Services (TNS) - Service Desk will reach out to you for whatever additional informaiton The Campaign Registry requires to approve your campaign.

Examples of variables that The Campaign Registry may require, based on your Brand:

- Campaign details
  - Brand: The brand associated with this campaign.
  - Description: A description for the campaign, explaining its purpose and target audience.
  - Call-to-Action / Message Flow: A description of how end users are expected to engage with this campaign (such as opt-in process, expected interaction).

- Campaign use cases
  - Content Type: The type of content you intend to send (such as Marketing or Customer Care).
  - Sub-content Type: A more specific content category if applicable.
  - Sample Message: A sample message that aligns with the campaign's use case. Multiple sample messages are acceptable.

- Campaign and content attributes
  - Subscriber Opt-in: Indication if subscriber opt-in is required.
  - Subscriber Opt-in Message: If opt-in is required, the message for subscribers to receive when opting into the campaign.
  - Subscriber Opt-out: Indicate if subscribers can opt out.
  - Subscriber Opt-out Answer: If opt-out is required, enter the response message for subscribers to receive when opting out.
  - Subscriber Help: Indicate if subscriber help is available.
  - Subscriber Help Answer: If help is available, provide the message for subscribers seeking assistance.

- Additional attributes
  - Direct Lending or Loan Arrangement: Indicates if the campaign involves any lending or loan arrangements.
  - Embedded Link: Specifies if the campaign includes an embedded link.
  - Embedded Phone Number: Specifies if a phone number is embedded within the campaign content.
  - Age-gated Content: Indicates if the content is age-restricted.

To initiate Campaign approval application, in the Teams Admin Center, navigate to ***Voice*** > ***Service configuration*** > ***SMS*** > ***Step 2: Create campaign***.

Select **Create Campaign / Update Campaign / View details** to open a right-side configuration slide-out and populate the fields with your company’s campaign information.
The ability to apply for Campaign approval will not be supported until the Brand is approved.

Populate your campaign application to The Campaign Registry according to the field headers as follows:

### Campaign description

In the campaign form, provide details of your company's plan for SMS operations, if any.

|Category |Description |
|:-----|:-----|
|Direct lending or loan arrangements related |Indicates whether the campaign includes content related to direct lending or other loan arrangements. |
|Embedded Link |Indicates whether the campaign is using an embedded link of any kind. Public URL shorteners (bitly, tinyurl) aren't accepted. |
|Embedded phone number |Indicates whether the campaign is using an embedded phone number (except the required HELP information contact phone number). |
|Age-gated content |Indicates whether the campaign includes any age-gated content as defined by Carrier and CTIA guidelines.|


### Microsoft Terms and Conditions

Select the box to accept the terms and conditions.

The terms as follows relate to Microsoft sharing your brand information with an operator, in this case, The Campaign Registry.

```text
Teams SMS services involve an integration between Microsoft and the underlying carrier, aggregator, or operator ("Operator"). Microsoft must share application details and/or brand information with the Operator to ensure that the program meets regulatory guidelines and standards set by operators. The Operator is the final reviewer and approver of your service application. If the details you provide on your application change, it's your responsibility to resubmit your application with up-to-date information. By submitting an application, you agree that Microsoft may share the application details as necessary for provisioning the Teams messaging service.
```

### Submitting and status

Select **Submit**.

Once submitted, the status indicates *"Submitted"* and the campaign information can’t be modified without Microsoft Support intervention.

The Service Level Agreement for campaign approval (or rejection) is seven days maximum.

If you submitted incorrect campaign information, if you haven't received approval or rejection notice in seven days, or if you have questions related to the process, [contact Microsoft's Telephone Number Services (TNS) - Service Desk](contact-tns-service-desk.md).

If The Campaign Registry rejects your campaign submission, a case is automatically opened on your behalf with Microsoft's Telephone Number Services - Service Desk. You can view your case by navigating to the [Phone Number Service Center](https://pstnsd.powerappsportals.com), and navigating to the tab for **My Company Cases**. Open the case, and you can interact with the Telephone Number Services - Service Desk team about the details and status of the case.

## Considerations

Because the Campaign application approval can be tedious, Microsoft is working to minimize the level of effort to get your Campaign approved. The following topics relate to considerations when preparing your SMS operation.

### The Campaign approval process

The Campaign Registry may require additional information from your company before approving your campaign. Potential items that may be required before approval:

- Further description details about your campaign's purpose
- Your company's privacy statement related to SMS messaging
- Your company's terms and conditions related to SMS messaging

If your company doesn't have a privacy statement or terms and conditions related to SMS messaging, you can use a Microsoft-provided template, completed with your company's information. For the template, see [SMS privacy statement and terms and conditions template](sms-privacy-terms-template.md).

If your campaign is rejected, be prepared to supply this information to Microsoft's Telephone Number Services team through the [Phone Number Service Center](https://pstnsd.powerappsportals.com).

### Opt-out messaging

In the initical Campaign application to The Campaign Registry, Microsoft will provide a generic campaign sample message, opt-in, opt-out, and help message. The default message that will be provided to The Campaign Registry (and first time recipients of Teams SMS messages) is as follows:

*"Hello, a user of Microsoft Teams sent you this message. If you don't want to get messages from this user anymore, reply STOP. To learn more about how to use messaging in Microsoft Teams, reply HELP."*

If a recipient responds with "STOP", all following messages from the Teams user's number will be blocked to that recipient.

If a recipient responds with "HELP", the recipient will be offered a url to a website of your discretion.

### Building a campaign with more than 49 SMS-enabled numbers

If you require more than 49 SMS-enabled numbers, you must work with [Microsoft's Telephone Number Services - Service Desk](contact-tns-service-desk.md) so that they can work with you on an exception to the default maximum campaign quantity. Provide the TNS Service Desk with the number of SMS-enabled numbers and the expected volume of messages sent and received per month, so that they can support the required provisioning.

## Related topics

[Microsoft Calling Plan Overview](calling-plan-overview.md)

[Getting numbers with Microsoft Calling Plan](manage-phone-numbers-landing-page.md)

[Learn about SMS texting in Teams](sms-overview.md)

[SMS privacy statement and terms and conditions template](sms-privacy-terms-template.md)

[Step 3: Enable SMS](sms-management.md)
