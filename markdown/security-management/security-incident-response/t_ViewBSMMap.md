---
title: Identify all configuration items affected by a security incident
description: If you know which resource \(server, desktop or other configuration item\) is behind a security incident and want to identify related resources and business services that can be affected, you can use the Business Service Management \(BSM\) map.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [View information in a security incident, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Identify all configuration items affected by a security incident

If you know which resource \(server, desktop or other configuration item\) is behind a security incident and want to identify related resources and business services that can be affected, you can use the Business Service Management \(BSM\) map.

## Before you begin

Role required: admin or sn\_si.admin

## About this task

The BSM map displays the upstream and downstream dependencies for a selected root CI.

There are two methods you can use to view the BSM map for a CI:

-   If you want to view CIs from the context of a task, view from the security incident form.
-   If you do not want to view CIs from a task viewpoint, view from the navigation bar.

## Procedure

1.  From the Security Incident form, populate the **Configuration item** field, and click the BSM map icon \(![Show CI map](../image/ShowCIMap.png)\).

    The BSM map screen displays the map for the last incident you accessed in Incident Management or the last security incident you accessed in Security Incident Management.

    ![BSM map](../image/BSMMap.png)

2.  Click the icons next to a configuration item to view different kinds of details about the resource \(server, desktop, or other CI\).

    For example, click \(![Alert icon](../image/AlertIcon.png)\) to view alerts associated with the CI.

    **Note:** To view a list of all the available icons, click **Filters** above the BSM map and expand **Filter Task Types**.

3.  To arrange the map in different configurations, select any of the formats listed above the map \(**Vertical**, **Horizontal**, **Radial**\), or click **Filters** to filter the map for easier viewing.

4.  If you opened the BSM map from the security incident form, you can add a dependent CI to the security incident by right-clicking the CI and selecting **Add Affected CIs**.

    You can also add multiple CIs at a time. Drag a box around the CIs you want to add, right-click the box, and select **Add Affected CIs**.

    The CIs are added to the Affected CIs related list of the security incident.


