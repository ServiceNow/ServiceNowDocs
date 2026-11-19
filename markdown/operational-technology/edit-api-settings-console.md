---
title: Editing API settings
description: Edit the API settings for the Discovery Console for OT to generate active tokens, remove denied tokens, or view the available API endpoints needed to communicate with the Service Graph Connector \(SGC\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/operational-technology/edit-api-settings-console.html
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Discovery Console for OT API, Settings page, Using the Discovery Console, Discovery Console for OT, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Editing API settings

Edit the API settings for the Discovery Console for OT to generate active tokens, remove denied tokens, or view the available API endpoints needed to communicate with the Service Graph Connector \(SGC\).

## Before you begin

Role required: admin

## About this task

The SGC has been enhanced to enable these functions of the Discovery Console for OT API.

## Procedure

1.  In the main menu, select the **Settings** page.

2.  On the **Settings** page, select the **API** tab.

3.  **Active Tokens**
4.  Under the **API** tab, to generate an API token, complete the following actions.

    1.  Select the **Active Tokens** tab.
    2.  Select the Add icon \[Omitted image "add-icon-msi.jpg"\] Alt text: Add icon.
    3.  In the Generate API Token window, select the expiration date.
    4.  Select **Generate Token**.
5.  **Remove Denied Tokens**
6.  To remove denied tokens, complete the following actions.

    1.  Select the **Denied Tokens** tab.
    2.  Next to the API token that you want to remove, select the **Remove Token** \[Omitted image "remove-token-icon-msi.png"\] Alt text: Remove icon.
7.  **Endpoints**
8.  To view the available endpoints, select the **Endpoints** tab.

    The endpoints are listed in columns by name, method, and their URI. The following endpoints are available for the Discovery Console for OT.

    -   Sites
    -   Assets: returns the `DeviceId` for each asset; if no `DeviceId` is set, then it returns `null`.
    -   Network Zones: returns values for the Network zone, parent/child zones, subnet information, and IP ranges.
    -   Sensors: returns the Sensor id \(`sensorId`\) that points to the sensor that was used for the discovery.
    -   Connections
    -   Installed Programs
    -   Images
    -   Sensor Health
    -   License Status: returns the status of the license and whether it is expired, to the Discovery Console for OT.
    -   Notifications
    \[Omitted image "settings-endpoints.png"\] Alt text: Endpoints

    1.  You can select the **Copy** icon to copy the endpoint.

    2.  The data is matched to the API.

    3.  Automatically stores files under `./apiexports`.

    4.  Use the naming convention `${API}_${DATE}.json` \(for example, `Assets_19791231.json`\).

    5.  After creating the new file, delete any previously created files.

    6.  Only generate files if there is sufficient disk space.

        The disk space available is limited to 1 GiB.


