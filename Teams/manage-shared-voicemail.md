---
title: "Manage Shared Voicemail"
author: mkbond007
ms.author: mabond
manager: pamgreen
ms.reviewer: vijurtse
ms.date: 1/16/2025
ms.topic: article
ms.tgt.pltfrm: cloud
ms.service: msteams
search.appverid: MET150
ms.collection:
  - M365-voice
  - m365initiative-voice
  - highpri
  - Tier1
audience: Admin
appliesto:
  - Microsoft Teams
  - Skype for Business
ms.localizationpriority: medium
f1.keywords:
- CSH
ms.custom:
  - Phone System
description: "Learn how to manage Shared Voicemail for your users."
---

# Manage Shared Voicemail

This article describes how to manage Shared Voicemail for your users. Shared Voicemail allows multiple users to access a single voicemail inbox.

## Overview

Shared Voicemail is an additional type of voicemail that complements personal voicemail. Shared voicemail is sent to a group of users, and any member of this group can access the message.

Shared Voicemail connects to Microsoft 365 Group and can be accessed from the Microsoft 365 Group's associated group folder in Outlook or through a Microsoft Teams Microsoft 365 Group's associated Teams Channel under the Calls section. Shared Voicemail also supports distribution lists and mail-enabled security groups, but we recommend using a M365 group.

Your users can receive Shared Voicemail through the redirection logic from Auto Attendants or Call Queues.

## Prerequisites

In order to manage Shared Voicemail, you must configure a Microsoft 365 Group with mailbox support. Specifically for Voicemail you could start with Teams or Outlook type groups.

Private and public group types work for Shared Voicemail. However, if the group is public, anybody in your organization will be able to view group related infomation. For more information about public and private groups, see [make-microsoft-365-groups-public-or-private](https://support.microsoft.com/office/make-microsoft-365-groups-public-or-private-c0a991b3-9c56-48b8-bf0f-05530f836b1b). For more information about M365 groups, see [office-365-groups](https://learn.microsoft.com/microsoft-365/admin/create-groups/office-365-groups)

A **Microsoft 365 group with Outlook type** has mailbox enabled by default, but this group might be missing Teams support. For more information, see [Create a group in Outlook](https://support.microsoft.com/office/create-a-group-in-outlook-04d0c9cf-6864-423c-a380-4fa858f27102)	

If your organization plans to view and manage Shared Voicemails within Microsoft Teams chats or other applications, you need to ensure that the relevant Microsoft 365 group has Microsoft Teams support. Voicemails that are stored in the Teams-supported groups will be accessible via Microsoft Teams by design.

A **Microsoft 365 group with a Microsoft Teams type** has the mailbox hidden by default. To make the mailbox visible, use the [Set-UnifiedGroup](/powershell/module/exchange/set-unifiedgroup) cmdlet with the `-HiddenFromExchangeClientsEnabled` parameter to make a mailbox visible.

  ```powershell
  Set-UnifiedGroup -Identity <GUID?> -HiddenFromExchangeClientsEnabled:$false
  ```

 If you select a Microsoft 365 group that is not supported by Teams, then your organisation will be able to manage voicemails addressed to this group only via Outlook, that eventually is going to have a more limited set of functionalities comparing to Teams interface.

For more information about creating a group in Teams, see [Microsoft 365 Groups and Microsoft Teams](/microsoftteams/office-365-groups). For information about creating a group in Outlook, see [Create a group in Outlook](https://support.microsoft.com/office/04d0c9cf-6864-423c-a380-4fa858f27102).



## Configure Shared Voicemail

Only members of the Microsoft 365 Group can access the Shared Voicemail. Each Shared Voicemail is associated with one Microsoft 365 Group.

Note: If you configure the call redirection logic so that multiple Call Queues  with different agents redirect calls to a common Shared Voicemail, all these users will need to be members of the Voicemail-associated Microsoft 365 Group to manage voicemails. This permission model could potentially lead to information oversharing. Therefore, it is recommended to set up a separate Shared Voicemail group for each specific Call Queue or Call Queue related security group. Ideally the Call Queue Microsoft 365 Group and the Voicemail Microsoft 365 Group should be the same group.  Similar techniques could also be applied to Auto Attendant scenarios.

Note: The recommendation is to use Microsoft 365 groups for Call Queue and Auto Attendant setup, that is the same as Voicemail groups to guarantee seamless integration with Shared Voicemail. 

For more information, visit [manage-your-call-queue-and-auto-attendant-settings-in-microsoft-teams](https://support.microsoft.com/office/manage-your-call-queue-and-auto-attendant-settings-in-microsoft-teams-52c741c6-8577-4faf-aa5a-c7853e0ab8f8)

### Auto attendants
You can setup redirection rules in Auto Attendant to forward calls to a Shared Voicemail. For detailed instructions, refer to the guide
[Set up a Microsoft Teams Auto attendant](https://learn.microsoft.com/microsoftteams/create-a-phone-system-auto-attendant)
For example, you might want to configure a rule to forward out-of-office hours calls to Shared Voicemail or to forward calls with a certain category directly to Shared Voicemail.

System greeting is available for Shared Voicemail calls from Auto Attendant. Option to supress the greeting is also available. Custom greetings are not yet available.

### Call queues
[Authorized users](https://learn.microsoft.com/microsoftteams/create-a-phone-system-call-queue?tabs=authorized-users#tabpanel_1_authorized-users) of a Call Queue can set up custom Shared Voicemail greetings.  
•	Shared voicemail greeting for call overflow
•	Shared voicemail greeting for call timeout
•	Shared voicemail greeting for no agents

Option to supress the greeting is also provided.
For instructions, refer to the guide [manage-voice-applications-policies](https://learn.microsoft.com/en-us/microsoftteams/manage-voice-applications-policies)
Note: Please avoid including any special characters in the greeting messages of Shared Voicemail. 

Redirection to Shared Voicemail under Call Queues is configured in the exception handling section. Refer to the
[Create a Call queue in Microsoft Teams](https://learn.microsoft.com/microsoftteams/create-a-phone-system-call-queue?tabs=call-exception-handling)

and [create-a-phone-system-call-queue](https://learn.microsoft.com/en-us/microsoftteams/create-a-phone-system-call-queue?tabs=call-exception-handling-additional-messaging)

## Explain Shared Voicemail access to your users
### Microsoft Outlook
Personal voicemails can typically be found in your personal Inbox or, in older versions of Outlook, under the “Voice mail” Search Folder. Shared voicemails, however, are located in the associated Group’s Folder Inbox.

Voicemails are essentially regular emails that include specific voicemail data and an audio file attachment. All voicemails are categorized with the type “Voicemail,” allowing you to apply rules to these messages. For instance, you can create a rule to move all messages categorized as “Voicemail” to a separate Outlook folder if needed. Outlook's functionality for regular emails also applies to voicemails, such as deleting, marking as read/unread, setting categories, applying flags, and more.

Below are some useful links:
- [Set categories, flags, or reminders - Microsoft Support](https://support.microsoft.com/office/set-categories-flags-or-reminders-a894348d-b308-4185-840f-aff63063d076))
- [Organize email by using folders in Outlook - Microsoft Support](https://support.microsoft.com/en-us/office/organize-email-by-using-folders-in-outlook-0616c259-4bc1-4f35-807d-61eb59ac79c1)
- [Set up rules in Outlook - Microsoft Support](https://support.microsoft.com/office/set-up-rules-in-outlook-75ab719a-2ce8-49a7-a214-6d62b67cbd41)

To get an automatic summary of voicemails more accurately using Outlook Copilot, it's recommended to organize voicemails in a separate folder. This way, you can ask Copilot to summarize new messages specifically in this folder.
### Microsoft Teams
Personal voicemails can typically be found in your personal Calls tab. Shared Voicemails can be found under Microsoft Teams Microsoft 365 Group's associated Teams Channel under the Calls section. 

## Related articles

[Set up Cloud Voicemail](set-up-phone-system-voicemail.md)

[Microsoft 365 Groups and Microsoft Teams](/microsoftteams/office-365-groups)

[Set-UnifiedGroup](/powershell/module/exchange/set-unifiedgroup)

[Create a group in Outlook](https://support.microsoft.com/en-us/office/04d0c9cf-6864-423c-a380-4fa858f27102)
