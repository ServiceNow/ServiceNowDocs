---
title: Configure response feedback
description: Configure the response feedback options that appear when users select thumbs up or thumbs down on a Now Assist in Virtual Agent or Now Assist panel response.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-31"
reading_time_minutes: 1
breadcrumb: [Configuring Now Assist Admin features, Now Assist, Enable AI experiences]
---

# Configure response feedback

Configure the response feedback options that appear when users select thumbs up or thumbs down on a Now Assist in Virtual Agent or Now Assist panel response.

## Before you begin

Role required: admin

## Procedure

1.  In the filter navigator field, enter `sys_now_assist_deployment_config_attributes.list` to display the Now Assist Deployment Config Attributes table.

2.  In the selection fields, select **Name** from the drop-down list and enter `granular` in the Search field.

3.  If you want to change whether negative granular feedback is enabled for Now Assist in Virtual Agent, select **is\_negative\_granular\_feedback\_enabled** that has Now Assist in Virtual Agent \(default\) as the Deployment Configuration.

4.  On the next screen, change the value to **true** if you want negative granular feedback to be enabled or to **false** if you do not want negative granular feedback to be enabled.

5.  Select **Submit**.

6.  If you want to change whether positive granular feedback is enabled for Now Assist in Virtual Agent, select **is\_positive\_granular\_feedback\_enabled** that has Now Assist in Virtual Agent \(default\) as the Deployment Configuration.

7.  On the next screen, change the value to **true** if you want positive granular feedback to be enabled or to **false** if you do not want positive granular feedback to be enabled.

8.  Select **Submit**.

9.  To configure the feedback options, in the filter navigator field, enter `sys_now_assist_message_bundle.list` to display the Now Assist Message Bundles table.

10. In the selection fields, select **for text** from the drop-down list and enter `granular` in the Search field.

11. Do one of the following:

    -   To create a new granular feedback selection, select **New**.
    -   To change an existing granular feedback option, select the option.
12. Enter or change the fields: Description, Message, Message Key, Bundle Id, Application, Active, Order.

13. Select **Submit**.

14. To access the stored feedback data, in the filter navigator field, enter `sys_ci_analytics.list` to display the CI Analytics table.

15. Select the appropriate entry to view the feedback data.


**Parent Topic:**[Configuring Now Assist Admin features](../../now-assist-admin/concept/configuring-na-landing.md)

