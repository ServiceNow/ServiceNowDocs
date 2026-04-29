---
title: Add application details
description: Add application details for your integration.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Add a integration, Use, LLM-powered SIR integration builder, Security Operations]
---

# Add application details

Add application details for your integration.

## Before you begin

Role required: sn\_si\_int\_kit.integration\_creator

## Procedure

1.  Navigate to **All** &gt; **Now Assist for Integration Toolkit** &gt; **SIR Integration Builder**.

2.  On the **Custom integrations** page, select **New**.

    You can also select an unpublished application to edit an integration. You can only view a published application.

3.  On the **Create new integration** page, select **Application type**.

    -   **Create new application**
        1.  Enter **Application name**.
        2.  Add a description about the integration.
        3.  Specify a unique **Scope name**. The maximum length of scope name must be 18 characters.

            **Note:** The scope name is of the `x_<company-code>_<unique_scope_name>` format. Where,

            -   x\_&lt;company-code&gt;\_: Auto-populated prefix for the scope name, which includes the company code mentioned in the "glide.appcreator.company.code" system property.
            -   &lt;unique\_scope\_name&gt;: Unique scope name for this integration.
        4.  Select **Create application**.
        5.  Select the ![](../images/browse.png) icon to view the details of the application.
        6.  To attach a logo for your integration, select **Upload logo**.

            ![Add application details screen](../images/application-details.png)

        7.  Select **Save changes**.
    -   **Choose existing application**
        1.  Select an existing application in **Select Application**.
        2.  Select **Save changes**.
4.  Select **Next** to add connection details.


