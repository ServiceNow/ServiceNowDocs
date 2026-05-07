---
title: Edit API settings
description: Edit the API settings for the Discovery Console for OT to generate active tokens, remove denied tokens, or view the available API endpoints needed to communicate with the Service Graph Connector \(SGC\).
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Discovery Console for OT API, Settings page, Use the Console pages, Discovery Console for OT, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Edit API settings

Edit the API settings for the Discovery Console for OT to generate active tokens, remove denied tokens, or view the available API endpoints needed to communicate with the Service Graph Connector \(SGC\).

## Before you begin

Role required: admin

## About this task

The SGC has been enhanced to enable these functions of the Discovery Console for OT API.

## Procedure

1.  In the main menu, go to the Settings page.

2.  On the Settings page, select the **API** tab.

3.  **Active Tokens**
4.  Generate an API token.

    1.  Select the **Active Tokens** tab.
    2.  Select the add icon ![](../image/add-icon-msi.jpg).
    3.  In the Generate API Token window, select the expiration date.
    4.  Select **Generate Token**.
5.  Remove denied tokens.

    1.  Select the **Denied Tokens** tab.
    2.  Next to the API token that you want to remove, select the **Remove Token** ![](../image/remove-token-icon-msi.png) icon.
6.  View the available endpoints.

    The endpoints are listed in columns by name, method, and their URI. The following endpoints are available for the Discovery Console for OT.

    -   **Sites**
    -   **Assets**: Returns the `DeviceId` for each asset; if no `DeviceId` is set, then it returns `null`.
    -   **Network Zones**: Returns values for the Network zone, parent/child zones, subnet information, and IP ranges.
    -   **Sensors**: Returns the Sensor id \(`sensorId`\) that points to the sensor that was used for the discovery.
    -   **Connections**
    -   **Installed Programs**
    -   **Images**
    -   **Sensor Health**
    -   **License Status**: Returns the status of the license and whether it is expired, to the Discovery Console for OT.
    -   **Notifications**
    ![Endpoints](../../operational-technology-discovery/images/settings-endpoints.png)

    1.  Select the **Endpoints** tab.

    2.  Select the copy icon \(![](../../operational-technology-discovery/images/copy-icon.png)\) to copy the endpoint.

    3.  The data is matched to the API.

    4.  Automatically store files under `./apiexports`.

    5.  Use the naming convention `${API}_${DATE}.json` \(for example, `Assets_19791231.json`\).

    6.  After creating the new file, delete any previously created files.

    7.  Only generate files if there is sufficient disk space.

        The disk space available is limited to 1 GiB.


