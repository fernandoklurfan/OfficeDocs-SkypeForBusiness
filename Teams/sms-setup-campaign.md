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
- Teams Communications Administrator
- Teams Telephony Administrator, or
- Global Admin

## Building a Campaign

The 10DLC (10-digit long code) registration process involves verifying your organization's intent and ability to use the 10DLC network in compliance. To get your intent approved, you submit a "Campaign" in the Teams admin center.

In the Teams Admin Center, navigate to ***Voice*** > ***Service configuration*** > ***SMS*** > ***Step 2: Create campaign***.
Select **Create Campaign / Update Campaign / View details** to open a right-side configuration slide-out and populate the fields with your company’s campaign information.

Populate your campaign application to The Campaign Registry according to the field headers as follows:

### Campaign description

In the campaign form, provide details of your company's plan for SMS operations, if any.

|Category |Description |
|:-----|:-----|
|Direct lending or loan arrangements related |Indicates whether the campaign includes content related to direct lending or other loan arrangements. |
|Embedded Link |Indicates whether the campaign is using an embedded link of any kind. Public URL shorteners (bitly, tinyurl) aren't accepted. |
|Embedded phone number |Indicates whether the campaign is using an embedded phone number (except the required HELP information contact phone number). |
|Age-gated content |Indicates whether the campaign includes any age-gated content as defined by Carrier and CTIA guidelines.|

### Terms and Conditions

When the fields are completed with accuracy, select the box to accept the terms and conditions.

The terms as follows relate to Microsoft sharing your brand information with an operator, in this case, The Campaign Registry.

```text
Teams SMS services involve an integration between Microsoft and the underlying carrier, aggregator, or operator ("Operator"). Microsoft must share application details and/or brand information with the Operator to ensure that the program meets regulatory guidelines and standards set by operators. The Operator is the final reviewer and approver of your service application. If the details you provide on your application change, it's your responsibility to resubmit your application with up-to-date information. By submitting an application, you agree that Microsoft may share the application details as necessary for provisioning the Teams messaging service.
```

### Submitting and status

Select **Submit**.

Once submitted, the status indicates *"Submitted"* and the campaign information can’t be modified without Microsoft Support intervention.

The Service Level Agreement for campaign approval (or rejection) is three days maximum.

If you submitted incorrect campaign information, if you haven't received approval or rejection notice in three days, or if you have questions related to the process, [contact Microsoft's Telephone Number Services (TNS) - Service Desk](contact-tns-service-desk.md).

If The Campaign Registry rejects your campaign submission, a case is automatically opened on your behalf with Microsoft's Telephone Number Services - Service Desk. You can view your case by navigating to the [Phone Number Service Center](https://pstnsd.powerappsportals.com), and navigating to the tab for **My Company Cases**. Open the case, and you can interact with the Telephone Number Services - Service Desk team about the details and status of the case.

## Considerations

The Campaign Registry may require additional information from your company before approving your campaign. Potential items that may be required before approval:

- Further description details about your campaign's purpose
- Your company's privacy statement related to SMS messaging
- Your company's terms and conditions related to SMS messaging

If your company doesn't have a privacy statement or terms and conditions related to SMS messaging, you can use a Microsoft-provided template, completed with your company's information. For the template, see [SMS privacy statement and terms and conditions template](sms-privacy-terms-template.md).

If your campaign is rejected, be prepared to supply this information to Microsoft's Telephone Number Services team through the [Phone Number Service Center](https://pstnsd.powerappsportals.com).

If you require more than 49 SMS-enabled numbers, you must work with [Microsoft's Telephone Number Services - Service Desk](contact-tns-service-desk.md) so that they can work with you on an exception to the default maximum campaign quantity. Provide the TNS Service Desk with the number of SMS-enabled numbers and the expected volume of messages sent and received per month, so that they can support the required provisioning.

## Related topics

[Microsoft Calling Plan Overview](calling-plan-overview.md)

[Getting numbers with Microsoft Calling Plan](manage-phone-numbers-landing-page.md)

[Learn about SMS texting in Teams](sms-overview.md)

[SMS privacy statement and terms and conditions template](sms-privacy-terms-template.md)

[Step 3: Enable SMS](sms-management.md)
