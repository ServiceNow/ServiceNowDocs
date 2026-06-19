---
title: Create import schedule
description: After importing sites and configuring site mappings, you can create an import schedule.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/sgcc-configure-import-schedule.html
release: australia
product: Operational Technology
classification: operational-technology
topic_type: task
last_updated: "2026-05-20"
reading_time_minutes: 1
breadcrumb: [SGC Central, Service Graph Connector for ServiceNow Operational Technology \(OT\) Discovery, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Create import schedule

After importing sites and configuring site mappings, you can create an import schedule.

## Before you begin

Role required: admin

## Procedure

1.  Do the **Configure scheduled jobs** task next.

    By default, the ServiceNow OT Discovery scheduled jobs created during installation are inactive. All other jobs are configured to run after their parent job, the Site Scheduled Data Import Job. The only exception is the Asset Image import jobs, which run independently.

    The following schedules jobs are available to import data:

    -   **Asset import**: This imports the OT Devices discovered into CMDB.
    -   **Network Zone import**: This imports the list of Managed Networks defined within the Site to support the deployment of OT Discovery.
    -   **Sensor import**: This imports list of all the Sensors used for OT Discovery deployment into the NIDS table.
    -   **Connection import**: This imports the list of communications between the devices.
    -   **Asset Images**: This imports the list of screenshots captured during the discovery process in the cmn\_media table.
2.  When done, select **Mark as complete**.

    \[Omitted image "sgcc-import-schedules-2.png"\] Alt text: IConfigure import schedules

3.  Navigate to **Confirm connection setup**.

4.  Check the connection setup to confirm it is valid.

5.  From this step you can select **View all connections**.

    \[Omitted image "sgcc-confirm-connection-setup-2.png"\] Alt text: Confirm connection setup


