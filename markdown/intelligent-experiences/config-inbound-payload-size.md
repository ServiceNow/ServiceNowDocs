---
title: Increase maximum inbound content length for scripted REST APIs
description: Increase the maximum allowed inbound content length for scripted REST APIs when automated agentic evaluation runs fail due to inbound payload size limitations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/config-inbound-payload-size.html
release: australia
topic_type: task
last_updated: "2026-06-09"
reading_time_minutes: 1
breadcrumb: [Reference, Evaluate agentic AI assets, AI Agent Studio, Enable AI experiences]
---

# Increase maximum inbound content length for scripted REST APIs

Increase the maximum allowed inbound content length for scripted REST APIs when automated agentic evaluation runs fail due to inbound payload size limitations.

## Before you begin

Role required: admin

## About this task

If evaluation runs fail due to inbound payload size limitations, you can increase the maximum allowed inbound content length for scripted REST APIs by modifying the system property **glide.rest.scripted.max\_inbound\_content\_length\_mb**. The default value is 10 MB. You can set this to 12 MB for moderately larger payloads or 25 MB for significantly larger payloads, or adjust to other values as required by your environment and governance policies.

**Note:** Increasing the inbound content limit may impact memory consumption and request processing. Review platform capacity and governance guidelines before setting higher values.

## Procedure

1.  Navigate to **System Definition** &gt; **System Properties**.

2.  Search for the property **glide.rest.scripted.max\_inbound\_content\_length\_mb**.

3.  Update the value from the default **10** to one of the following:

    -   **12** MB for moderately larger payloads
    -   **25** MB for significantly larger payloads
4.  Save the changes.

5.  Re-run the evaluation.


