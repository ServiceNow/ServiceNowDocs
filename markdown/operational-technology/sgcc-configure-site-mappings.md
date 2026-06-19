---
title: Configure site mappings
description: Importing the site data must be complete before you can move onto configure site mappings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/sgcc-configure-site-mappings.html
release: australia
product: Operational Technology
classification: operational-technology
topic_type: task
last_updated: "2026-05-20"
reading_time_minutes: 1
breadcrumb: [SGC Central, Service Graph Connector for ServiceNow Operational Technology \(OT\) Discovery, Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Configure site mappings

Importing the site data must be complete before you can move onto configure site mappings.

## About this task

Before proceeding, review and configure imported ServiceNow OT discovery site mapping records and verify that the site data has been fully imported via the site scheduled data import. The site mapping records will not be available unit the import is complete.

## Before you begin

Role required: admin

## Procedure

1.  In the **Configure site mappings** task, scroll down to review the list of imported sites.

    \[Omitted image "sgcc-configure-site-mappings.png"\] Alt text:

2.  Select the first site and in the form that opens, fill in the fields as follows.

    \[Omitted image "window-confgurei-site-mappings-1.png"\] Alt text: Configure site mappings

    1.  All field titles with \* \(asterick\) next to them are mandatory and should be filled in.

    2.  Select a value in the **Site type** field.

        The value can be either **OT** or **IT**. If you select **OT**, all hardware records imported later also have OT device \(**cmdb\_ot\_entity**\) records related to them automatically. For any site with a site type between IT and OT, select **OT**.

    3.  Select an **ISA assignment site**.

        All data in the site imports to the ISA assignment site you select.

    4.  If applicable, populate the **Location** and **Company** fields.

    5.  Check the **Active** box.

    **Note:** Any value populated is cascaded down to all configuration items \(CIs\) this Site is related to when the asset data is imported into the CMDB.

3.  Select **Continue** to move to the next step.


