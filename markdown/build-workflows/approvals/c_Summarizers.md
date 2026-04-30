---
title: Summarizers
description: Approval summarizers are stored in the Macro \[sys\_ui\_macro\] table.
locale: en-US
release: zurich
product: Approvals
classification: approvals
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Approval summarizer formatter, Classic approvals, Build workflows]
---

# Summarizers

Approval summarizers are stored in the Macro \[sys\_ui\_macro\] table.

From the left navigation pane, select **System UI** &gt; **UI Macros**. Summarizers use a naming convention of approval\_summarizer\_ + '&lt;table\_name&gt; \(for example, approval\_summarizer\_change\_request is the summarizer for change requests, while approval\_summarizer\_sc\_request is the summarizer for service catalog requests\).

Each summarizer is written in Jelly script, which is used to define internal forms. The script is stored in the large XML field at the bottom of the UI Macro form.

