---
title: Now Assist for Zero Copy Connector workflow troubleshooting
description: Use generative AI logs and Workflow Studio to troubleshoot issues with Now Assist for Zero Copy Connector agentic workflows.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Use agentic AI, Now Assist for Zero Copy Connector, Workflow Data Fabric]
---

# Now Assist for Zero Copy Connector workflow troubleshooting

Use generative AI logs and Workflow Studio to troubleshoot issues with Now Assist for Zero Copy Connector agentic workflows.

The first troubleshooting option is to view generative AI logs.

1.  Select **All** enter `sys_generative_ai_log_list.do` in the **Filter**, and press **enter** or **return** on your keyboard.
2.  Open any record to view details.

A second option is to enable a system property and use Workflow Studio. The com.glide.oneapi.flow\_debug property enables debugging capabilities for flows built with OneAPI so you can receive reporting and insights into flow execution.

1.  Select **All** enter `sys_properties.list` in the **Filter**, and press **enter** or **return** on your keyboard.
2.  Search for and open the property named **com.glide.oneapi.flow\_debug**.
3.  Check that the **Value** is set to **True**.
4.  After the property is enabled, use Workflow Studio to check executions.

    ![Workflow studio operations tab, with two executions highlighted.](../images/erp-data-explorer-workflow6.png)

    For more information, see Workflow Studio.


