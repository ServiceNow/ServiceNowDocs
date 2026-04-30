---
title: Configure a communications template for SMS in Major Incident Management
description: Configure a communication template for SMS in Major Incident Management to help reduce the efforts and time spent in creating and composing communication SMS.
locale: en-US
release: yokohama
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up communication templates and plans in Major Incident Management, Configuring Major Incident Management in Service Operations Workspace, Setting up Major Incident Management in Service Operations Workspace, Getting started with Service Operations Workspace for ITSM, Configure, Service Operations Workspace for ITSM, IT Service Management]
---

# Configure a communications template for SMS in Major Incident Management

Configure a communication template for SMS in Major Incident Management to help reduce the efforts and time spent in creating and composing communication SMS.

## Before you begin

Major Incident Management must be installed and activated in Service Operations Workspace. For more information, see [Activate Major Incident Management in Service Operations Workspace](install-mim-sow.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** &gt; **Configurations**.

2.  On the Admin Center page, navigate to the configuration page for Major Incident Management through either the **Overview** tab or the **Configurations** tab.

    -   In the **Overview** tab, select **Configure** for Major Incident Management.
    -   In the **Configurations** tab, select **Major Incident Management**.
    The configuration page displays all configurable features in Major Incident Management.

3.  In the **Communications Template** section, select **Configure SMS**.

    The Notify SMS template page displays a list of available communication SMS templates. For more information on Notify, see [Notify](https://www.servicenow.com/docs/access?context=notify-landing-page&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

4.  Select **New**.

5.  On the form, fill in the details.

<table id="table_o4l_4hw_y1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the SMS template.

</td></tr><tr><td>

Table

</td><td>

Table on which the SMS template is used.

 **Note:** By default, the value is the Incident Communication Task \[incident\_alert\_task\] table.

</td></tr><tr><td>

Template

</td><td>

Content added in the body of the SMS.

</td></tr><tr><td>

Select Variables

</td><td>

Field variables added to the **Template**.

</td></tr></tbody>
</table>6.  Select **Submit**.

    The SMS template record is added to the list of available communication SMS templates.


