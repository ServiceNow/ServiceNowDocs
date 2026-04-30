---
title: Create configuration values for risk impact
description: Use the Risk Impact module to create configuration values for the impact vector.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing risks scores in Enterprise Asset Management, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Create configuration values for risk impact

Use the Risk Impact module to create configuration values for the impact vector.

## Before you begin

Role required: sn\_eam.enterprise\_admin

## Procedure

1.  Navigate to **Enterprise Asset Workspace** &gt; **Admin center** &gt; **Risk configuration** &gt; **Risk impact**.

2.  Select **New**.

3.  Enter a label in the Enterprise Risk Impact Configuration page.

    The **Value** field is an incremental field and cannot be edited.

4.  Select **Submit**.

    The **Display Name** field is automatically populated and is a concatenation of the value and the label. For example, if 1 is the value and Low is the label, the **Display Name** field appears as `1-Low`.

5.  To add more configuration values, repeat steps 2-4.

    There should be a minimum of three impact records and a maximum of ten.

6.  Select **Freeze** after you have added the configuration records.

7.  Select **OK** in the warning message box to continue freezing your configuration records.

    **Note:** You cannot add or delete any impact configuration records after you select **Freeze**. You can however edit the **Label** field in the existing records.


**Parent Topic:**[Managing risks scores in Enterprise Asset Management](../concept/managing-eam-risk-scores.md)

