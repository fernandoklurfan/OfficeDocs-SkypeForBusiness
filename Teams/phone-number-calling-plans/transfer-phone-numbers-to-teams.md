---
title: Transfer phone numbers to Microsoft Teams
author: sfrancis206
ms.author: scottfrancis
manager: pamgreen
ms.reviewer: leiaglezer
ms.date: 03/26/2024
ms.topic: article
ms.tgt.pltfrm: cloud
ms.service: msteams
audience: Admin
f1.keywords:
- NOCSH
ms.collection: 
  - M365-voice
  - m365initiative-voice
  - highpri
  - Tier1
appliesto: 
  - Microsoft Teams
ms.localizationpriority: medium
search.appverid: MET150
description: Submitting a port request. Learn how to transfer telephone numbers to Microsoft for Calling Plans in Teams.
ms.custom: seo-marvel-mar2020
---

# Submitting a port request

This article is and accompaniment for IT professionals and Teams Phone administrators in the process of porting phone numbers to Microsoft Calling Plans.

**Prerequisites**

1. Review the information in [Planning number ports](port-order-overview.md)
2. Gather related documentation.

**Optional methods for porting**

There are two options for transferring numbers to Microsoft.

1. Self-fulfillment process using the wizard in Teams Admin Center
2. Manual request process through Microsoft's Phone Number Service Center

A third option for U.S. and Canada, and being developed to support all countries, is a new wizard experience.

>
> [!NOTE]
> You ***must*** submit a **manual** port request, if you're porting the following types of numbers
>
> • Port requests with a quantity of more than 999 numbers
>
> • Audio conferencing bridge numbers
>
> • Auto attendants or other service numbers
>
> • Toll-free phone numbers

## Create a port order and transfer your phone numbers to Teams

### [**New porting wizard**](#tab/new-porting-wizard)

>
> [!NOTE]
> This is the accompnaniment for porting numbers in U.S. and Canada. Use the classic porting wizard accompaniment for all other regions.

1. In Teams Admin Center, launch the port wizard
    1. In the left navigation rail, go to **Voice** > **Phone numbers**. Select **Numbers**, and then select **Port**.

2. The wizard’s splash screen allows you to select the location for the numbers you wish to port.
    * If you're porting U.S. or Canada numbers and choose **US & Canada**, you're automatically triaged into the new porting wizard.  
    * To continue, select **US & Canada**

#### Get started

1. Review the information on the Get started page, and then from the drop-down, Select the country or region currently hosting the telephone numbers to be ported.

2. When you specify a country or region, the wizard calls out the documents from the current carrier that you need to complete your port order.

3. Make note of these documents required for later steps.

#### Phone numbers

1. Add your phone numbers manually or by uploading a list.
    * To add phone numbers manually, enter numbers in 10-digit or E.164 format, separated by a comma or semi-colon. Ranges aren't supported. Optional dashes or hyphens are supported.
    * To upload a list of phone numbers, the list must be in CSV format and must have only one column with a header designated as PhoneNumber. Each phone number must be in a separate row and can be in 10-digit or E.164 format.

2. Upon adding phone numbers, the wizard compiles the numbers, categorize them, and then display a table of the numbers in groups by *account*, *service provider*, and *type*.
    * The wizard allows you to select one of the groups for processing. The wizard only processes a port request with one type of group at a time.
    * If the wizard categorized your numbers into more than one group, you must submit a separate port request for each. See [Planning number ports](port-order-overview.md)
    * Select the desired group of numbers and **Continue with selection**.

#### Billing telephone number (BTN)

1. The Billing telephone number (BTN) for the phone numbers being ported must match what the current service provider has on file for the account. Also, if there's a freeze on the account it must be removed. If the BTN is incorrect or there's a freeze on the account, your port request is rejected.
    * The BTN should be in **E.164 format**
    * The BTN can also be referred to as the 'Account telephone number.' It's the primary phone number associated with your account. Your service provider uses the BTN to track activities, payments, and customer service records.
    * You can usually find your BTN on an account statement. If you're unsure, ask your current service provider's account representative to help you identify your BTN.
    * In a full port request, all numbers associated with the BTN are ported to Microsoft, including the BTN, and the respective account with the current provider is closed.
    * In a partial port request, you have two scenarios:
        * You are porting only the phone numbers previously specified, not including the BTN which stays in service with the current provider.
        * You are porting only a portion of the account's phone numbers, including the BTN. In this case, designate one of the numbers being left behind to become the replacement BTN.

#### Account information

1. As with the BTN, it's essential to document the account information exactly the way the current service provider has it in their records. 

    *Don't forget to save your work as you work through this page.*

    * The organization name should match, exactly as represented in the current service provider's records.
    * If the wizard identifies the service provider's name, don't change it here.
    * The account  number should be discoverable on an account statement or invoice, or in your provider's online account portal.
    * The account may have an account PIN and if so, it must be provided here. The account PIN isn't the same as a BTN Freeze PIN. A BTN Freeze PIN allows an authorized user to unfreeze an account for maintenance, such as porting activities. The account PIN is used for security, to prevent unauthorized access to account management and records. The *account* PIN is required in this step.
    * The authorized user is one or more persons associated with the account and is authorized for account management and records. Only one authorized user needs to be designated on your port request. If you're unsure of the account's authorized user, contact your service provider's account manager.
    * The service address is specific to the phone numbers that you're porting. If you're porting numbers for multiple sites, input the address for all sites here. The service addresses defined here also functions as the default emergency address.

#### Documents

1. Upload the recommended articles from your service provider
    * Files should be in .pdf format
    * Files are stored within your tenant and shared with Microsoft's Telephone Number Service Center.
    * The Requester details translate to the authorized user for the telephone numbers, once they're ported to Microsoft.

#### Porting details

1. Indicate the specifics for your Microsoft service.
    * The order name becomes viewable by you in the Teams Admin Center during the porting process and after order completion for your records.
    * For the port details, remember to review [Planning number ports](port-order-overview.md).
    * If adding multiple email addresses for more contacts, separate with a semi-colon.

#### Authorize and submit

1. You have two options for submitting.
    1. Sign with e-signature (recommended)
        1. In this case, an email is sent to the current *authorized user* that you specified in **Account information** page, and they're prompted to authorize with Microsoft's e-signature tool.
        1. Once the authorized user approves, the request is automatically submitted to Microsoft.
    1. Offline signature.
        1. In this case, you download the Letter of Authorization, get it signed, upload it, and submit to Microsoft.

#### Confirmation

1. Confirmation of the request is acknowledged within 72 business hours.
1. You can check the status of your order in the Teams Admin Center. In left side rail under Voice > Phone Numbers navigate to **Order History** and search by the name you gave your order in the porting details page.
1. You can research more about the process, here: [Porting status](port-order-status.md)

### [**Classic porting wizard**](#tab/classic-porting-wizard)

1. In Teams Admin Center, launch the port wizard
    1. In the left navigation rail, go to **Voice** > **Phone numbers**. Select **Numbers**, and then select **Port**.

2. The wizard’s splash screen allows you to select the location for the numbers you wish to port.
    * If you're porting U.S. or Canada numbers and choose **US & Canada**, you're automatically triaged into the new porting wizard.  
    * Otherwise, for U.S. or Canada and all other regions, follow this classic process. Enhancements are in development to offer the new wizard to all other regions where Microsoft offers Calling Plans.
    * To continue, select **All other supported regions**.

#### Get started

On the **Get started** page, populate the fields per your request.

**Country or region**: Country or region where you're porting numbers.
**List your phone number** Add your phone numbers manually or by uploading a list.
* To add phone numbers manually, enter numbers in 10-digit or E.164 format, separated by a comma or semi-colon. Ranges aren't supported. Optional dashes or hyphens are supported.
* To upload a list of phone numbers, the list must be in CSV format and must have only one column with a header designated as PhoneNumber. Each phone number must be in a separate row and can be in 10-digit or E.164 format.

#### Manage numbers

The Manage numbers page provides an initial check to make sure the number format is recognized by the wizard, matches the country or region you specified, and is a valid number.
If the number validation summary isn't successful, check the number and country or region and try again. Otherwise, continue.

#### Add account information

On the **Add account information** page, complete the following, and then select **Next**.
>
> [!NOTE]
> The information displayed on this page is determined by the country or region and number type. Each country and region has different regulations on the information that's required to port numbers. What you see on this page may be different from what's described here.

**Order details**:

This is where you input your port request details.

The order name you specify here becomes viewable by you in the Teams Admin Center during the porting process and after order completion for your records.

In the **Port details**, enter the Billing Telephone Number (BTN) in E.164 format.
- If you enter a BTN number that isn't in the list of numbers that you're porting, your request is automatically categorized as a **Partial port** and the BTN will remain with your current service provider after the port is complete.
- If you enter a BTN number that matches a number in the list of numbers that you're porting, you have two options.
    * Port **all numbers in my account**. If you choose this option, the account with your current service provider will be closed after the port is complete.
    * Port **some numbers in my account, and I'm including my account's BTN**. If you choose this partial port option, you can enter a new BTN to designate for the account that is still open with your current service provider.

In the **Organization details**, enter your organization's name.

In the **Current service provider details**, provide the current service provider's name, account number and security PIN.

In the **Requester details**, populate this information with the contact details of the person who shall be the authorized user with Microsoft once the numbers are ported.
   
In the **Authorized user details**, populate this information with the contact details of the person who is the authorized user with your current service provider.'

In the **How do you want to sign the Letter of Authorization?** section, you select whether you will use e-signature or manual upload for the Letter of Authorization.

In the **Service address**, assign the default emergency address for the numbers.

In the **Default number usage** section, you select the intended typed of usage for the numbers. If you would like to change it, select *Yes, change usages* to go to **Add number features** page. If you select *No*, you will skip to the **Complete your order** page.

#### Add number features

The add number features page is where you update the number usage. Usage is a category of service for the phone numbers.

For numbers assigned to users, the default number type is geographic phone numbers and is listed as **User**.

For numbers assigned to voice applications, such as Auto-Attendants and Call Queues, the number usage type should be set as **Voice app**.

For numbers assigned to audio conferencing, the number usage type should be set to **Conference**.

Toll-free numbers default to **Voice app**, but you can make changes to the default number usages in this section of the wizard.

To update the number usage, check the desired number and select **Update number usage**. Then, from the right-hand side rail, use the drop-down and select your desired number usage to assign to the numbers.

#### Complete your order

If you selected **Paper signature** in the **Add account information** page, you can download a Letter of Authorization template.

* The template is prepopulated with the information you input in the wizard. 
* Once signed, you upload an electronic copy of the signed Letter of Authorization and then you can select **Submit** and the port request proceeds.

If you selected **E-signature** in the **Add account information** page, the authorized user receives an email to sign the Letter of Authorization once you select **Complete and send e-signature request**. 
* Once they electronically sign, the port request proceeds.

### [**Manually submit port request**](#tab/manually-submit-port-request)

In some situations, you may have to manually submit a service request to get phone numbers, transfer phone numbers, release phone numbers, or change addresses. To see the requirements for each country and region or to learn more about number porting, see [Manage phone numbers for your organization](../manage-phone-numbers.md)

Use the steps in this article to manually submit a port order if you're unable to use the porting wizard.

#### Manually submitting a new port order

1. Upload your completed Letter of Authorization (LOA) form directly to the Phone Number Service Center.
    * Download the [Letter of Authorization](../manage-phone-numbers.md) for your country or region.
    * Complete the form.
    * Send it to the [Phone Number Service Center](../manage-phone-numbers-for-your-organization/contact-tns-service-desk.md)

---

## What happens next

When we receive your port order, you receive an email that verifies your request. Your request is updated daily, and you're notified of its progress and status in email. If your current carrier rejects the port request, contact the [Phone Number Service Center](../manage-phone-numbers-for-your-organization/contact-tns-service-desk.md) for assistance.

To view the status of your port order, in the left navigation of the Microsoft Teams admin center, go to  **Voice** > **Port orders**, and then select **Order history**. Each port order status is listed in the **Status** column. To learn more, see [What's the status of your port orders?](port-order-status.md)

For more information about Letters of Authorization to port existing phone numbers and other considerations, see [Manage phone numbers for Calling Plan](../manage-phone-numbers-for-your-organization.md) and [Planning number ports](port-order-overview.md)

## Report phone number issues

If you notice any issues with the ported numbers within the first 24-48 hours after the port is completed, contact the [Phone Number Service Center](../manage-phone-numbers-for-your-organization/contact-tns-service-desk.md). For any issues beyond 48 hours, contact the Microsoft Support Team.

## Related articles

- [Planning number ports](port-order-overview.md)
- [Different kinds of phone numbers used for Calling Plans](../different-kinds-of-phone-numbers-used-for-calling-plans.md)
- [Manage phone numbers for your organization](../manage-phone-numbers-for-your-organization/manage-phone-numbers-for-your-organization.md)
- [Emergency calling terms and conditions](../emergency-calling-terms-and-conditions.md)
- [Emergency Calling disclaimer label](https://download.microsoft.com/download/9/9/0/990e24c1-eb49-4b52-9306-dbd4c864ed91/emergency-calling-label-(en-us)-(v.1.0).zip)
