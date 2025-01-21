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

Shared Voicemail is an additional type of voicemail that complements personal voicemail. Shared voicemail is assigned to a group of users, and any member of this group can access the messages.

Shared Voicemail connects to Microsoft 365 Group and can be accessed from the Microsoft 365 Group's associated group folder in Outlook or through a Microsoft Teams Microsoft 365 Group's associated Teams Channel under the Calls section. Shared Voicemail also supports distribution lists and mail-enabled security groups, but we recommend using a M365 group.

Your users can receive Shared Voicemail directly from a call to an Microsoft 365 group (for example, via Microsoft Teams) or through the redirection logic from Auto Attendants or Call Queues.

## Prerequisites

In order to manage Shared Voicemail, you must configure a Microsoft 365 Group for Outlook or Teams.

Private and public group types work for Shared Voicemail. However, if the group is public, anybody in your organization can access voicemails. If the group is private, only members of the group can access voicemails.

If your organization plans to view and manage Shared Voicemails within Microsoft Teams chats or other applications, you need to ensure that the relevant Microsoft 365 group has Microsoft Teams support. Only voicemails that are stored in the Teams-supported groups are visible via Microsoft Teams.

A **Microsoft 365 group with a Microsoft Teams type** has the mailbox hidden by default. To make the mailbox visible, use the [Set-UnifiedGroup](/powershell/module/exchange/set-unifiedgroup) cmdlet with the `-HiddenFromExchangeClientsEnabled` parameter to make a mailbox visible.

  ```powershell
  Set-UnifiedGroup -Identity <GUID?> -HiddenFromExchangeClientsEnabled:$false
  ```

If you select a Microsoft 365 group that isn't supported by Teams, then your organization can only manage voicemails associated with that group in Outlook.

For more information about creating a group in Teams, see [Microsoft 365 Groups and Microsoft Teams](/microsoftteams/office-365-groups). For information about creating a group in Outlook, see [Create a group in Outlook](https://support.microsoft.com/en-us/office/04d0c9cf-6864-423c-a380-4fa858f27102).

## Configure Shared Voicemail

As an admin, you can configure Shared Voicemail for......

Only members of the Microsoft 365 Group can access the Shared Voicemail. Each Shared Voicemail is associated with one Microsoft 365 Group.

### Auto attendants

### Call queues

## Related articles

[Set up Cloud Voicemail](set-up-phone-system-voicemail.md)

[Microsoft 365 Groups and Microsoft Teams](/microsoftteams/office-365-groups)

[Set-UnifiedGroup](/powershell/module/exchange/set-unifiedgroup)

[Create a group in Outlook](https://support.microsoft.com/en-us/office/04d0c9cf-6864-423c-a380-4fa858f27102)
