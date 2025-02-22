---
title:  Update monitoring in the Teams admin center
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
description: Monitoring for updates for the Teams client using the Teams admin center.
appliesto: 
- Microsoft Teams
ms.localizationpriority: medium
---

# Microsoft Teams update monitoring

[!INCLUDE [new-feature-teams-admin-center](includes/new-feature-teams-admin-center.md)]

As an admin, it’s important that your users have the latest and the most secure version of the Teams client. Teams update monitoring in the Teams admin center allows you to proactively monitor Teams client updates and versions and helps identify users who aren't on latest version of Teams, so you can support them.

This dashboard highlights the client update status for the devices in your tenant and gives Microsoft recommended insights for moving users to the latest version of Teams client.

## Access the Teams update dashboard

To access the update monitoring and insights dashboard:

1. Go to the Teams admin center. XXX PERMISSIONS HERE?
1. Select **Teams client health** from the navigation pane. XXX DIRECTIONALLY WHERE, YOU CAN'T JUST RELY ON THE SCREENSHOT.
XXX NEEDS MORE DETAIL. IMAGINE YOU'RE DESCRIBING THIS TO SOMEONE OVER THE PHONE.

:::image type="content" source="media/teams-client-health-main-page-alt.png" alt-text="A screenshot of the Teams client health page with callouts marked. The first callout is over the page title. The second callout is on the upper middle of a table showing details. The number three is to the upper right of this table next to search, settings, and export options.":::

- Callout 1: The Client update widget displays the overall version status distribution for all devices in your tenant. The update status widget provides statuses by 3 categories:
  - Latest Build: A device is running a Teams client build newer than the last 100% released build.
  - One or more builds behind: A device is running a Teams client build less than 30 days old and older than the last stable build.
  - Outdated: A device is running a Teams client build less than 90 days old and more than 30 days old.
- Callout 2: The table under the **Health tab** shows a more detailed breakdown of this information, such as:
  - Client versions: The exact client version number.
  - Release Date: The date this specific client version was fully released to the general ring.
  - Version status: The Teams client version status.
  - Platform: The platform for the client version.
  - Devices on this version: The total devices in the tenant currently running this client version.
  - Users on this version: The total number of users in the tenant currently running this client version.
  - Percentage of total users: The percentage of total users in the tenant currently running the client version.
  - Device Crashes: The total number of devices that experienced a client crash in the last 28 days.
  - Device launch failures: The total number of devices that experienced a client launch failure in the last 28 days.
- Callout 3: You can use these buttons to:
  - Export the table to a CSV file.
  - Filter and search by versions.
  - Manage settings for columns in the table.

### Client version details

You can see your organization's client version distribution and adoption of each client version, as well as the health of each client version in your organization. To view a detailed dashboard with insights, select any version from the health table from a row in this table.

You can identify users and devices running outdated version of Teams, and review troubleshooting insights on issues preventing users from updating to a newer version of Teams.

:::image type="content" source="media/teams-client-version-details-page.png" alt-text="A screenshot of the version details page, with callouts. The first callout, on the top left-hand side, is the client version. The second callout, underneath the first, is the date of release. The third callout, to the immediate right of the second, is the Teams client version. The fourth callout, in the middle underneath the third, has charts showing trends. The fifth, center of the screenshot, shows a table with details. The sixth, to the middle right, shows search, settings, and export options.":::

- Callout 1: Client versions - The exact client version number.
- Callout 2: Release Date - The date this specific client version was fully released to the general ring.
- Callout 3: Version status - The Teams client version status.
- Callout 4:
  - Devices on this version trend: The trend of devices adopting this client version the last 28 days.
  - Device crashes trend: The trend of devices experiencing client crashes on this version in the last 28 days.
  - Device launch failure trend: The trend of devices experiencing client launch failures on this version in the last 28 days.
- Callout 5:
  - The table provides the following data:
    - User: The username.
    - Ring: The ring that the user is currently using.
    - Device: The device name
    - Platform: The platform the user is running Teams client on.
    - Platform details: Operating system details.
    - Insight: If the user experienced an update failure and is running an outdated versions of Teams.
    - Last Activity: The timestamp of the last active update.
- Callout 6: You can search or filter for any client versions. You can also sort and export the dashboard's table in a CSV file that you can share.

## Client health per user

You can also monitor Client health per user from the user’s page.

1. Go to **Teams** > **Users** > **Manage users** page.
1. Select any user account.
1. Select the **Client health** tab.

:::image type="content" source="media/teams-client-per-user-view.png" alt-text="A screenshot of the per-user view, with numbered callouts. The first callout is slightly to the right of the middle of the screenshot, over the Client health tab. The second callout is directly underneath the first, above a table. The third is on the middle right of the screenshot, above the search, settings, and export options.":::

The client health tab provides breakdown of this information, including:

- Client versions: The exact client version number.
- Release Date: The date on which this specific client version was fully released to the general ring.
- Version status: The client version status of the Teams client version running on.
- Devices: The device name the user is currently running this Teams client on.
- Device Crashes: The total crashes experienced by this client version on the user’s specific device in the last 7 days.
- Device launch failures: The total launch failures experienced by this client version on the user's specific device in the last 7 days.
