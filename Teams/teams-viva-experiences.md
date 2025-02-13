---
title: Manage Viva Engage experiences in Microsoft Teams
author: DaniEASmith
ms.author: danismith
manager: jtremper
ms.reviewer: luises
ms.topic: how-to
ms.date: 02/13/2025
ms.service: msteams
audience: admin
ms.collection: 
- M365-collaboration
ms.custom:
- admindeeplinkTEAMS
search.appverid: MET150
f1.keywords:
- NOCSH
appliesto: 
- Microsoft Teams
ms.localizationpriority: medium
description: Learn about how to manage Viva Engage experiences in Microsoft Teams in chats.
---

# Manage Viva Engage experiences in Microsoft Teams

> [!NOTE]
> This feature is currently in public preview with Viva Engage storylines only.

Viva Engage unites your organization, allowing people to connect with leaders, coworkers, and communities. With Viva Engage, your users can generate ideas, share their work and experience, and find connection at work.

And, now Viva Engage can integrate into your users' Teams chats.

This article outlines the technical details of the integration of Viva Engage experiences in Teams chats and instructs IT admins on how they can manage this feature.

## Technical details for Viva Engage experiences in Teams

### Prerequisites for Viva Engage experiences in Teams

Before rolling out Viva Engage experiences to your users' Teams chats, ensure the following items:

- Your tenant isn't blocking [Viva Engage's IPs and URLs](/microsoft-365/enterprise/urls-and-ip-address-ranges).
- Sign-ins for the Office 365 Viva Engage service are enabled in Microsoft Entra ID.
  - Sign in to the [Microsoft Entra admin center](https://go.microsoft.com/fwlink/p/?linkid=2067268).
  - Go to **Identity** > **Applications** > **Enterprise Applications** > **Viva Engage** > **Properties**.
  - For the **Enabled for users to sign-in?** option, select **Yes**.

### User requirements for Viva Engage experiences in Teams

In order for users to access Viva Engage experiences in Teams, they must meet the following requirements:

- Be assigned a Microsoft 365 license
- Be assigned a Teams license
- Have access to [Viva Engage either with or without Viva Engage license enforcement](/viva/engage/setup#set-up-licensing-for-viva-engage)

### Current limitations of Viva Engage experiences in Teams

In the following list, find the current limitations of Viva Engage experiences in Teams:

- Assigning leaders in Viva Engage can only be done in the Viva Engage app.
- Assigning and managing delegates can only be done in the Viva Engage app.
- Campaigns and Topics pages can only be managed in the Viva Engage app.

### Data handling of Viva Engage experiences in Teams

Viva Engage content in Teams is handled by Viva Engage's data handling and compliance standards. To learn more about Viva Engage's data handling, see [Data, Privacy, and Security for Microsoft 365 Copilot in Viva Engage](/viva/engage/manage-security-and-compliance/data-privacy-security-copilot-engage).

## How to turn off and on Viva Engage experiences in Teams

The **Viva Engage experiences in Teams** messaging setting is turned **On** by default for your entire organization.

To change this setting, complete the following steps:

1. Sign in to the [Teams admin center](https://go.microsoft.com/fwlink/p/?linkid=2066851) with your admin credentials.
1. In the left-rail menu, select **Settings & policies**.
1. Select either **Global (Org-wide default) settings** or **Custom policies for users & groups**.
1. Scroll to the **Messaging** section and select **Messaging**.
1. On the **Messaging settings** page, find the **Viva Engage** section.
1. Switch off or on the **Viva Engage experiences in Teams** toggle.
1. Select the **Save** button.

## User experience of Viva Engage in Teams chats

The first Viva Engage experience to integrate with Teams chats is [storylines](/viva/engage/eac-storyline).

Storyline pages can be accessed in Teams chats with the following capabilities:

- Users can create new storyline posts directly from Teams.
- Users can follow, view, and comment on others' storylines in Teams.
- Users can sort storyline posts by most recent and recent activity.
- Users receive notifications in Teams for relevant activity in storylines.
- Storyline conversations have a look and feel similar to other messaging experiences in Teams.

If users have [Viva Engage Premium](/viva/engage/setup#set-up-licensing-for-viva-engage), they receive the following extra capabilities:

- Users can change the cover photo at the top of their storyline.
- Users can view personal analytics about their storyline.

## Related articles

- [Manage messaging policies in Teams](messaging-policies-in-teams.md)
- [Introducing Microsoft Viva Engage](/viva/engage/overview)
- [Manage and set up storyline in Viva Engage](/viva/engage/eac-storyline)
