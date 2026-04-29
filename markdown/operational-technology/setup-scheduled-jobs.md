---
title: Set up scheduled import jobs
description: Configure the scheduled import jobs.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Service Graph Connector for ServiceNow Operational Technology\(OT\) Discovery, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Set up scheduled import jobs

Configure the scheduled import jobs.

## Before you begin

Role required: admin

## Procedure

1.  In the Setup scheduled import jobs section select **Import sites**.

    1.  Next to the Import sites task, select **Configure**.
    2.  Select the Site Scheduled Data Import Job.
    3.  To manually execute the job, select **Execute Now**.
    4.  Return to the Guided Setup and select **Mark as complete** next to the Import sites task.
    5.  Next in the Configure site mappings task, select **Configure**.
    6.  Review the list of imported sites.
    7.  Select the first site and in the form, fill in the following fields.
        -   All field titles with \* \(asterick\) next to them are mandatory and should be filled in.
        -   Populate the **Site type** field. This field is mandatory. The value can be either OT or IT. If you select OT, all the hardware records imported later will also have OT device \(cmdb\_ot\_entity\) records related to them automatically. For any site with a Site type between IT and OT, set the **Site type** to **OT**.
        -   Set the ISA assignment site. All the data in the site will import to the ISA assignment site you choose.
        -   If applicable, populate the **Location** and **Company** fields.
        -   Check the Active box.
        -   Fill in the **Assigned Meta Data** section. Whatever you assign as Meta Data will be copied onto all imported devices.

            **Note:** Any value populated will be cascaded down to all CIs this Site is related to when the asset data is imported into the CMDB.

    8.  Select **Update**.
    9.  Return to the Guided Setup and select **Mark as complete**.
2.  Do the Configure scheduled jobs task next.

    By default, the ServiceNow OT Discovery scheduled jobs created during installation are inactive. All other jobs are configured to run after their parent job, the Site Scheduled Data Import Job. The only exception is the Asset Image import jobs, which run independently.

    1.  Next to the Configure scheduled job task, select **Configure**.
    2.  In the Scheduled Jobs list, open a site record.
    3.  To activate the scheduled job, select the check box next to the **Active** field.
    4.  In the **Run** and **Time** fields, select how often and when you want the job to run.

        For example, daily at midnight.

    5.  Select **Update**.
    6.  Repeat these steps for each site in the Scheduled Jobs list.
    7.  When you finish the sites, select the asset record from the Scheduled Jobs list.
    8.  To activate the scheduled job, select the check box next to the **Active** field.

        **Note:** You don't need to set the **Run** field for the asset record since the asset scheduled job automatically runs after the site scheduled job runs.

        The following schedules jobs are available to import data:

        -   **Asset import**: This imports the OT Devices discovered into CMDB.
        -   **Network Zone import**: This imports the list of Managed Networks defined within the Site to support the deployment of OT Discovery.
        -   **Sensor import**: This imports list of all the Sensors used for OT Discovery deployment into the NIDS table.
        -   **Connection import**: This imports the list of communications between the devices.
        -   **Asset Images**: This imports the list of screenshots captured during the discovery process in the cmn\_media table.
    9.  Return to the Guided Setup and select **Mark as complete** next to the Configure scheduled job task.
3.  Review imported data.

    1.  Wait until the scheduled jobs are complete on their schedule or open the scheduled job and select **Execute Now** to execute it on demand.
    2.  Once the jobs are complete, select **Configure** next to the Review imported data task.
    3.  Review the imported CMDB data.
    4.  Return to the Guided Setup and select **Mark as complete** next to the Review imported data task.

## Result

You have completed the Service Graph Connector for ServiceNow OT Discovery Guided Setup. You may want to review the [Use advanced configurations](advanced-configuration-sgc-ot-discovery.md) section.

