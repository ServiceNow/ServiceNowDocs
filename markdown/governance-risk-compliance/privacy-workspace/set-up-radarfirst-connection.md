---
title: Set up the RadarFirst connection
description: Create the connection and credential that allows Privacy Case Management to communicate with RadarFirst.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/privacy-workspace/set-up-radarfirst-connection.html
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-07-23"
reading_time_minutes: 2
keywords: [RadarFirst, connection, credential]
breadcrumb: [Configure, Integrate with RadarFirst, Privacy Case Management, Privacy Management, Governance, Risk, and Compliance]
---

# Set up the RadarFirst connection

Create the connection and credential that allows Privacy Case Management to communicate with RadarFirst.

## Before you begin

-   Role required: System administrator
-   Install the Privacy Case Management integration with RadarFirst \(sn\_privacy\_rf\) plugin, which provides the following default records:
    -   **RadarFirst Integration Configuration**, which is the connection and credential alias required to establish and authorize an HTTPs connection with RadarFirst.

        You must obtain a bearer key from your account administrator for authorization.

    -   **RadarFirst configuration**, which will be used to import RadarFirst data, and then map it to the breach assessment data in your instance.

## Procedure

1.  Open the guided setup by navigating to **All** &gt; **Privacy Case Management** &gt; **RadarFirst Integration** &gt; **RadarFirst Integration Guided Setup**.

2.  On the Welcome to Guided Setup landing page, select **Continue**.

3.  Select **Start** on the **Connections** step of the setup.

4.  Complete the Create new connection &amp; credential activity.

    1.  On the **Connection &amp; Credential Aliases** record, select the **Create New Connection &amp; Credential** link within the Related Links section.

        **Note:** Alternatively, navigate to **All** &gt; **IntegrationHub** &gt; **Connection &amp; Credential Aliases**, and select **RadarFirst Integration Configuration**. This opens the same **Connection &amp; Credential Aliases** record that you must update to complete this activity of the guided setup.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |**Connection Name**|Auto-filled. Name of the new connection. For example, `RadarFirst Integration Connection`.|
        |**RadarFirst Base URL**|Auto-filled. RadarFirst API address. For example, `https://api.radarfirst.com`|
        |**RadarFirst Integration Bearer Token**|Authentication key for the RadarFirst API connection request.|

    3.  Select **Create**.

        This creates a new HTTPS connection with RadarFirst, which will be used to import and map its data to the data elements and breach factors in Privacy Case Management.\[Omitted image "pcm-rf-new-connection.png"\] Alt text: The new HTTPs RadarFirst Integration Connection, which will be used to import data from RadarFirst.

    4.  On the Create new connection &amp; credential activity of the guided setup, select **Mark as complete**.

5.  Complete the Validate credentials activity.

    1.  On the **RadarFirst configuration** record, select **Validate credentials**.

        **Note:** Alternatively, navigate to **All** &gt; **Privacy Case Management** &gt; **RadarFirst Integration** and select **RadarFirst Configuration**. This opens the same **RadarFirst configuration** record where you must validate the credentials to complete this activity.

        If validation succeeds, the validation status updates to Valid credentials. If it fails, the **Observation** field highlights the errors.

    2.  On the Validate credentials activity of the guided setup, select **Mark as complete**.


## What to do next

Import RadarFirst data into your instance. See .

