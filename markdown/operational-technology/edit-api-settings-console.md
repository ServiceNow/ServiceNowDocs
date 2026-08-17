---
title: Edit API settings
description: Edit the API settings for the Discovery Console for OT to generate active tokens, remove denied tokens, or view the available API endpoints needed to communicate with the Service Graph Connector for ServiceNow OT Discovery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/edit-api-settings-console.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Discovery Console for OT API, Settings page, Use the Console pages, Discovery Console for OT, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Edit API settings

Edit the API settings for the Discovery Console for OT to generate active tokens, remove denied tokens, or view the available API endpoints needed to communicate with the Service Graph Connector for ServiceNow OT Discovery.

## Before you begin

Role required: admin

## About this task

The Service Graph Connector for ServiceNow OT Discovery has been enhanced to make available these functions of the Discovery Console for OT API.

## Procedure

1.  In the main menu, go to the Settings page.

2.  On the Settings page, select the **API** tab.

    \[Omitted image "settings-page-api-tab1.png"\] Alt text: API tab on the Settings page

3.  **Active Tokens**
4.  Generate an API token.

    1.  Select the **Active Tokens** tab.
    2.  Select the add icon \[Omitted image "add-icon-msi.jpg"\] Alt text:.
    3.  In the Generate API Token window, select the expiration date.
    4.  Select **Generate Token**.
5.  Remove denied tokens.

    1.  Select the **Denied Tokens** tab.
    2.  Next to the API token that you want to remove, select the **Remove Token** \[Omitted image "remove-token-icon-msi.png"\] Alt text: icon.
6.  View the available endpoints.

    The endpoints are listed in columns by name, method, and their URI. The following endpoints are available for the Discovery Console for OT.

    \[Omitted image "Settings-api-active-tokens.png"\] Alt text: API Endpoints

    -   **Sites**
    -   **Assets**: Returns the `DeviceId` for each asset; if no `DeviceId` is set, then it returns `null`.
    -   **Network Zones**: Returns values for the Network zone, parent/child zones, Subnet information, and IP ranges.
    -   **Sensors**: Returns the Sensor id \(`sensorId`\) that points to the sensor that was used for the discovery.
    -   **Console Info**: Returns the Console information.
    -   **Connections**
    -   **Connections-V2**
    -   **Installed Software**
    -   **Images**
    -   **Sensor Health**
    -   **License Status**: Returns the status of the license and whether it is expired, to the Discovery Console for OT.
    -   **Notifications**
    1.  Select the **Endpoints** tab.

    2.  Select the copy icon \(\[Omitted image "copy-icon.png"\] Alt text:\) to copy the endpoint.

    3.  The data is matched to the API.

    4.  Automatically store files under `./apiexports`.

    5.  Use the naming convention `${API}_${DATE}.json` \(for example, `Assets_19791231.json`\).

    6.  After creating the new file, delete any previously created files.

    7.  Only generate files if there is sufficient disk space.

        The disk space available is limited to 1 GiB.


**Parent Topic:**[Discovery Console for OT API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/operational-technology/api-discovery-console.md)

