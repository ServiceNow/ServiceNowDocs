---
title: Configure granular feedback options
description: Configure granular feedback options for Now Assist in Virtual Agent by manually editing the tables.
locale: en-US
release: australia
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2026-03-01"
reading_time_minutes: 1
breadcrumb: [Using Now Assist in Virtual Agent, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Configure granular feedback options

Configure granular feedback options for Now Assist in Virtual Agent by manually editing the tables.

## Before you begin

Role required: admin

## Procedure

1.  To enable or disable granular feedback, in the filter navigator field, enter `sys_now_assist_deployment_config_attributes.list`.

    The Now Assist Deployment Config Attributes table appears.

2.  In the selection fields, select **Name** from the drop-down list and enter `granular` in the Search field.

3.  If you want to change whether negative granular feedback is enabled for Now Assist in Virtual Agent, select **is\_negative\_granular\_feedback\_enabled** that has Now Assist in Virtual Agent \(default\) as the Deployment Configuration.

4.  On the next screen, change the value to **true** if you want negative granular feedback to be enabled or to **false** if you do not want negative granular feedback to be enabled.

5.  Select **Submit**.

6.  If you want to change whether positive granular feedback is enabled for Now Assist in Virtual Agent, select **is\_positive\_granular\_feedback\_enabled** that has Now Assist in Virtual Agent \(default\) as the Deployment Configuration.

7.  On the next screen, change the value to **true** if you want positive granular feedback to be enabled or to **false** if you do not want positive granular feedback to be enabled.

8.  Select **Submit**.

9.  To configure the feedback options, in the filter navigator field, enter `sys_now_assist_message_bundle.list`.

    The Now Assist Message Bundle table appears.

10. In the selection fields, select **Name** from the drop-down list and enter `granular` in the Search field.

11. Do one of the following:

    -   To create a new granular feedback selection, select **New**.
    -   To change an existing granular feedback option, select the option.
12. To access the stored feedback data, in the filter navigator field, enter `sys_ci_analytics.list`.

    The CI Analytics table appears.

13. Select the appropriate entry to view the feedback data.


