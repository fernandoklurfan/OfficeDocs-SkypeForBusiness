---
title:  Teams client supportability and manageability tools in Teams admin center health
ms.author: heidip
author: MicrosoftHeidi
manager: jtremper
ms.topic: article
ms.date: 01/31/2025
ms.service: msteams
audience: admin
ms.collection: 
- M365-collaboration
- m365initiative-deployteams
ms.reviewer: daro
search.appverid: MET150
f1.keywords:
- NOCSH
description: How to configure and use the health page in the Teams admin center to manage clients using monitoring and informational advice specific to situations.
appliesto: 
- Microsoft Teams
ms.localizationpriority: medium
---

# Teams client supportability and manageability tools in Teams admin center health

This article provides an overview of the new Teams Client Health Dashboards and tools for managing Teams clients in the Microsoft Teams admin center.

Teams client health is an all-new page with a set of data, insights, and tools to help administrators troubleshoot and resolve issues. When a Teams application experiences an issue, end-users typically reach out to their adminis. As an admin, you may be regularly occupied with requests from end-users. This in can leave you in a reactive position with limited information to diagnose and resolve problems effectively.

As an admin, you may need to proactively monitor, or you may need to perform remediation actions to manage and fix issues before they impact your end user productivity or cause further escalations.

## Teams client health

[XXX EMPTY SECTION WITH ONLY SCREENS]

## Teams update monitoring

- Teams update monitoring in the Teams admin center allows administrators to proactively monitor Teams client updates and versions, and helps identify users who aren't on the latest version of the Teams client.
- Admins can monitor the overall update and adoption status of the latest version of the Teams client across Windows and Mac devices in their organization. 
- This page provides a Teams client update status from users in your organization. It groups devices into three update statuses:
  - Latest Build
  - One or more builds behind
  - Outdated

|Client update status      |Definition |
|--------------------------|-----------|
|Latest build              |If a device is running a Teams client build newer than the last 100% released build. |
|One or more builds behind |If a device is running a Teams client build less than 30 days old and older than the last stable build, it's **One or more builds behind**. |
|Outdated                  |If a device is running Teams client build less than 90 days old and more than 30 days old, it's identified as **Outdated**. |

- The **Health tab** shows different data information, such as:
  - Client versions, their release date, version status, and platform.
  - Devices on this version.
  - Users on this version.
  - Percentage of total users.

- Health Metric:
  - Device crashes
  - Device launch failures

### Client version details

Admins can see their organization's client version distribution and adoption of each client version, as well as the health of each client version.

[SCREENSHOT NOT CURRENTLY INCLUDED]

Identify users and devices running outdated version of Teams. Review troubleshooting insights on issues preventing users from updating to a newer version of Teams.

## Get diagnostic logs


