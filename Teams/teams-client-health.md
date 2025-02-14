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
ms.reviewer: shals
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

Teams client health is an all-new page with a set of data, insights, and tools to help administrators troubleshoot and resolve issues. When a Teams application experiences an issue, end-users typically reach out to their admins. As an admin, you may be regularly occupied with requests from end-users. This can leave you in a reactive position with limited information to diagnose and resolve problems effectively.

As an admin, you may need to proactively monitor, or you may need to perform remediation actions to manage and fix issues before they impact your end user productivity or cause further escalations.

## Access the Teams Client health dashboard

To access the update monitoring and insights dashboard, follow these steps:

1. Go to the Teams admin center.
1. Select **Teams client health** from the navigation pane.

The Teams client health page displays an overview of Teams client health along with more information when you go into the details.

XXX SCREENSHOT
ALT TEXT FOR SCREENSHOT: A screenshot of the client health page with four callout boxes marked. Box 1 is in the top center of the page next to Client health. Box 2 is on the top right next to Top issues. Box 3 is on the lower left next to Items and Filtered by. Box 4 is on the lower right next to the filter box.

The **Client health** widget displays key health metrics like device crashes and launch failure trends for the last 28 days for all devices in your tenant.

> [!NOTE]
> This widget only surfaces health markers that are end-user impacting and actionable by administrators.
 
More details on each metric displayed are listed below:

- Callout 1: This widget shows Client health trends across the health metric below:
    - **Crashes**: The number of devices experiencing Teams app crashes per day within the last 28 days. Supported for Windows (non-VDI) and Mac Applications.
    - **Launch failures**: The number of devices experiencing Teams app launch failures per day within the last 28 days.
    > [!NOTE]
    > This is supported for Windows (non-VDI) and Mac applications.
- Callout 2: This widget shows the top issues experienced by users in the organization:
    - Device reported crashes: The number of devices that experienced crashes in the last 7 days. The number of devices that experienced crashes in last 28 days.
    - Device reported launch failures: The number of devices that experienced launch failures in the last 7 days. The number of devices that experienced launch failures in the last 28 days.
    - Device reported update failures: The number of devices that experienced update failures in last 7 days. The number of devices that experienced update failures in last 28 days.
- Callout 3: This table provides the following data:
    - Issue: Problems impacting devices and users in the tenant.
    - Insights: Insights on potential reasons behind these problems.
    - Impacted Devices in the last 7 days (%): The number of devices that experienced the issue in the last 7 days and the percentage of the device base impacted in the organization.
    - Affected users in the last 7 days (%): The number of users who experienced the issue in the last 7 days and the percentage of the user base impacted in the organization.
    - Impacted Devices in the last 28 days (%): The number of devices that experienced the issue in the last 28 days and the percentage of the device base impacted in the organization.
    - Affected users in the last 28 days (%): The number of users who experienced the issue in the last 28 days and the percentage of the user base impacted in the organization.
    - Suggested Actions: Recommended mitigation guidance to troubleshoot and fix the issue. 
- Callout 4: You can use these buttons to:
    - Export the table to a CSV file.
    - Filter by Issue or Insight.
    - Access settings for the columns in the table.

XXX SCREENSHOT

- Callout 1: Issue Type - The category of issue impacting users and devices.
- Callout 2: Insight - The insight or reason leading users and devices to experience the issue.
- Callout 3: Mitigation link - This link points to Microsoft recommended mitigation and guidance to resolving the issue.
- Callout 4: The table provides the following data:
    - Client Version - The Teams client version the user is currently on.
    - Version Status - The client version status of the Teams client the user is running on.
    - Ring - The ring the user is a part of.
    - Device - Details about the device the user is currently using.
    - Device crashes - The number of devices that experienced crashes in last 7 days.
    - Device launch failures - The number of devices that experienced launch failures in the last 7 days.
    - Updated on (UTC) - The time stamp when this information was last refreshed.
- Callout 5: You can use these buttons to:
    - Export the table to a CSV file.
    - Filter and search by versions.
    - Manage settings for columns in the table.

