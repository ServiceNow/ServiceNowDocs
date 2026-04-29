---
title: Populate Cloud Account Management dependent tables
description: Provide the required information for cloud account creation and provisioning.
locale: en-US
release: australia
product: Cloud Account Management
classification: cloud-account-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up Cloud Account Management in Cloud Workspace, Configuring Cloud Account Management, Cloud Account Management, ITOM Cloud Accelerate, IT Operations Management]
---

# Populate Cloud Account Management dependent tables

Provide the required information for cloud account creation and provisioning.

## Before you begin

Role required: sn\_itom\_cam.cw\_admin

## Procedure

1.  Add environment elements to help categorize cloud accounts based on multiple environments.

    1.  Navigate to **All** and search for `sys_choice.LIST`.

    2.  On the Choice page, select **Element** from the drop-down list and enter `environment` in the search field.
    3.  If environment elements you want to use do not exist, create them.

        1.  Select **New**.
        2.  On the form, fill in the required fields.

            |Field|Value|
            |-----|-----|
            |Table|Choice \[sys\_choice\] table|
            |Element|`environment` \(case sensitive\)|
            |Label|The name for the environment you want to appear on the cloud account request page, for example, Production.|
            |Value|The same value as the label.|

        3.  Select **Submit**.
2.  Populate the remaining tables.

    1.  Navigate to **All** and search for the table name.

    2.  Add the relevant information.

<table id="table_jln_4yr_dfc"><thead><tr><th>

Table name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Environment \(sys\_choice\)

</td><td>

Contains translated text for options that appear in lists.

</td></tr><tr><td>

Cost Center \(cmn\_cost\_center\)

</td><td>

Contains commonly used reference between financial systems and IT. Cost center records represent business entities and have a related list of CI Cost Center Relationships that measure the cost center's consumption of business services.

</td></tr><tr><td>

Business Unit \(business\_unit\)

</td><td>

Contains information on the business units within your organization, including functions like Finance, HR, or IT.

</td></tr><tr><td>

Department \(cmn\_department\)

</td><td>

Contains the names of the departments in your organization.

</td></tr><tr><td>

System User \(sys\_user\)

</td><td>

Contains user information for the ServiceNow instance.

</td></tr></tbody>
</table>
