---
title: Summarizers
description: Approval summarizers are stored in the Macro \[sys\_ui\_macro\] table.
locale: en-US
release: yokohama
product: Approvals
classification: approvals
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Approval summarizer formatter, Classic approvals, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Summarizers

Approval summarizers are stored in the Macro \[sys\_ui\_macro\] table.

From the left navigation pane, select **System UI** &gt; **UI Macros**. Summarizers use a naming convention of approval\_summarizer\_ + '&lt;table\_name&gt; \(for example, approval\_summarizer\_change\_request is the summarizer for change requests, while approval\_summarizer\_sc\_request is the summarizer for service catalog requests\).

Each summarizer is written in Jelly script, which is used to define internal forms. The script is stored in the large XML field at the bottom of the UI Macro form.

-   **[Change an approval summarizer](../task/t_ChangeASummarizer.md)**  
You can modify existing approval summaries to include additional information.
-   **[Create a new custom approval summarizer](../task/t_CreateANewCustomSummarizer.md)**  
After you add a new table that has approvals to an instance, you can add a custom activity formatter by creating a new UI macro and then add it to the appropriate form.

**Parent Topic:**[Approval summarizer formatter](../reference/r_ApprovalSummarizerFormatter.md)

