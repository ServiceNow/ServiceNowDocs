---
title: Create an instance and set the import schedule
description: Create an instance and determine when and how often you want your connector to import data.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Creating your own API connector, Use the workspace, Security Posture Control, Security Operations]
---

# Create an instance and set the import schedule

Create an instance and determine when and how often you want your connector to import data.

## Before you begin

Role required: sn\_sec\_spc\_core.developer

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Posture Control** &gt; **Connectors and use case setup**.

2.  Select the **SPC API Integrations** tab.

3.  Locate the card for your connector with the integrations used for mitigation controls data.

4.  Look for connectors with `CXF` in the name and select the card.

5.  Select **New** to create an instance.

6.  In the New instance modal, enter a unique name and select **Create Instance**.

7.  With the integration tile selected, select the instance you created in the previous step in the Name column.

8.  In step one in the modal, enter the alias and connection information and select **Next**.

9.  In step two in the modal, set how often and when you want the integration to import data.

10. Select **Save and exit**.

11. Add instances for the integration.

    Add more instances for the integration. The alias and connection credentials you created during the setup permit you to share credentials across multiple instances \(accounts\). You can have a maximum of five active instances for your API Integration.

12. To view and edit the import schedule, navigate to **All** &gt; **System Import Sets** &gt; **Administration** &gt; **Scheduled imports**.


