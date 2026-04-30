---
title: Configure to download the Microsoft Teams transcript
description: Configure how the Notify Connector for Microsoft Teams processes and stores meeting transcripts in ServiceNow.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-12-07"
reading_time_minutes: 1
breadcrumb: [Accessing Microsoft Teams meeting transcripts, Configure Notify connector, Microsoft Teams integration for Agent Experience, Configure, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Configure to download the Microsoft Teams transcript

Configure how the Notify Connector for Microsoft Teams processes and stores meeting transcripts in ServiceNow.

## Before you begin

Role required: Notify Teams admin

## Procedure

1.  Navigate to **All** &gt; **Notify** &gt; **Administration** &gt; **Microsoft Teams** &gt; **Configuration**.

2.  In the Setup tab, select the **Enable Events API** checkbox.

    **Note:** Events API is required for transcript retrieval. Without it, transcript functionality will not work.

    Perform sanity testing before switching from OnlineMeeting to Events API.

3.  Select **Update**.

4.  In the Transcript tab, select one of the following options:

    -   -   Do not process or store the transcript: ServiceNow will not retrieve or store any transcript information.
-   Store only the link to the transcript: ServiceNow stores a reference URL. Users can retrieve transcripts on demand using the Fetch Recording button.
-   Download and store the transcript as attachment: ServiceNow automatically retrieves and stores the complete transcript file.
5.  Select **Update**.


**Parent Topic:**[Accessing Microsoft Teams meeting transcripts](../concept/teams-meeting-transcript.md)

