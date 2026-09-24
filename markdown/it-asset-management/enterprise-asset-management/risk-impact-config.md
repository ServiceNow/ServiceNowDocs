---
title: Create configuration values for risk impact
description: Use the Risk Impact module to create configuration values for the impact vector.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/enterprise-asset-management/risk-impact-config.html
release: brazil
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring risk, Configure, Enterprise Asset Management, Asset Management]
---

# Create configuration values for risk impact

Use the Risk Impact module to create configuration values for the impact vector.

## Before you begin

Role required: sn\_eam.enterprise\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Enterprise Asset Workspace**.

2.  From the Enterprise Asset Workspace, open the Admin center view.

3.  From the navigation panel of the Admin center view, navigate to **Risk configuration** &gt; **Risk impact**.

4.  Select **New**.

5.  Enter a label in the Enterprise Risk Impact Configuration page.

    The **Value** field is an incremental field and cannot be edited.

6.  Select **Submit**.

    The **Display Name** field is automatically populated and is a concatenation of the value and the label. For example, if 1 is the value and Low is the label, the **Display Name** field appears as `1-Low`.

7.  To add more configuration values, repeat steps 2-4.

    There should be a minimum of three impact records and a maximum of ten.

8.  Select **Freeze** after you have added the configuration records.

9.  Select **OK** in the warning message box to continue freezing your configuration records.

    **Note:** You cannot add or delete any impact configuration records after you select **Freeze**. You can however edit the **Label** field in the existing records.


**Parent Topic:**[Managing risk in Enterprise Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/enterprise-asset-management/managing-eam-risk-scores.md)

