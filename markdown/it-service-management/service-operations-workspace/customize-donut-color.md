---
title: Configure the donut color in the Overview section
description: Create a visual experience that works the best for donuts in the Overview section.
locale: en-US
release: zurich
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Landing page configurations in Service Operations Workspace for ITSM, Getting started with Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure the donut color in the Overview section

Create a visual experience that works the best for donuts in the **Overview** section.

## Before you begin

Role required: sn\_sow\_admin.sn\_sow\_admin, or admin

## About this task

Donut area colors are based on the element that the donut is grouped by.

-   Tier-1 landing page
    -   In the **Incidents assigned to me** card, the donut is grouped by the state of incidents.
    -   In the **Unassigned incidents** card, the donut is grouped by the priority of incidents.
    -   In the **Catalog tasks assigned to me** card, the donut is grouped by the state of catalog tasks.
    -   In the **Incident SLAs** card, the donut is grouped by the time left after which the incidents will breach SLA.
-   Tier-2 landing page
    -   In the **Incidents assigned to me** card, the donut is grouped by the state of incidents.
    -   In the **Problems assigned to me** card, the donut is grouped by the state of problems.
    -   In the **Changes assigned to me** card, the donut is grouped by the state of change requests.
    -   In the **Tasks assigned to me** card, the donut is grouped by the state of catalog tasks.

## Procedure

1.  To change the donut area colors for the following cards in the tier-1 landing page, perform these steps.

    -   Incidents assigned to me
    -   Unassigned incidents
    -   Catalog tasks assigned to me
    1.  Navigate to **Reports** &gt; **Administration** &gt; **Chart Colors**

    2.  In the Chart Colors list, filter records based on the card that you want to customize and select a record.

        1.  To customize the color of the **Incidents assigned to me** card, filter records with **Name** as **incident** and **Element** as **state**.
        2.  To customize the color of the **Unassigned incidents** card, filter records with **Name** as **incident** and **Element** as **priority**.
        3.  To customize the color of the **Catalog tasks assigned to me** card, filter records with **Name** as **sc\_task** and **Element** as **state**.
    3.  On the Chart Colors form, select the required color in the **Color name** field.

    4.  Click **Update**.

2.  To change the donut area color for the Incident SLAs card in the tier-1 landing page, perform the following steps.

    1.  Navigate to **Reports** &gt; **Administration** &gt; **Report Ranges**.

    2.  In the Ranges list, filter records with **Name** as **task\_sla** and **Element** as **time\_left**.

    3.  Select the required record.

    4.  On the Range form, select the required color in the **Color name** field.

    5.  Click **Update**.

3.  To change the donut area colors for the tier-2 landing page, perform the following steps.

    1.  Navigate to **Reports** &gt; **Administration** &gt; **Chart Colors**

    2.  In the Chart Colors list, filter records based on the card that you want to customize and select a record.

        1.  To customize the color of the **Incidents assigned to me** card, filter records with **Name** as **incident** and **Element** as **state**.
        2.  To customize the color of the **Problems assigned to me** card, filter records with **Name** as **problem** and **Element** as **state**.
        3.  To customize the color of the **Changes assigned to me** card, filter records with **Name** as **change\_request** and **Element** as **state**.
        4.  To customize the color of the **Tasks assigned to me** card, filter records with **Name** as **sc\_task** and **Element** as **state**.
    3.  On the Chart Colors form, select the required color in the **Color name** field.

    4.  Click **Update**.


**Parent Topic:**[Landing page configurations in Service Operations Workspace for ITSM](../concept/landing-page-configurations-sow-itsm.md)

