---
title: Step 2. Create a view for modal window for a Security Case
description: Create a view for modal window for a Security Case.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Rollup example use case implementation for a Security Case, Rollup Framework for MSIM, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Step 2. Create a view for modal window for a Security Case

Create a view for modal window for a Security Case.

## Before you begin

**Key Consideration:**

-   By default, the linked record modal list will only be showing the **Default** list layout. If you want to customize the list layout, you can do so using **Custom View** on the Source Table.
-   If you want to render the custom view, the custom view should also be selected in the Linked Record Configuration for Source Table.

    ![Custom view is rendered to the Source Table.](../image/modal-view-image-step2.png "Modal view Linked Record Configuration for Source Table")


Role required: admin

## Procedure

1.  Go to the source table and click **Configure** &gt; **List Layout**.

    ![Configuring list layout and creating a new view name.](../image/configure-list-layout-view-name.png)

2.  Go to **List view** &gt; **View name**.

3.  Click **New** in the View name drop-down list and create a new view, for example, msim\_sn\_ti\_case\_modal\_view.

4.  Select the newly created view.

    Once selected, you can choose the required fields from the Available list.

5.  Click **Save**.

6.  Navigate to **Menu** &gt; **Views** to verify if the view has rendered properly.


**Parent Topic:**[Rollup example use case implementation for a Security Case](../concept/use-case-for-a-security-case.md)

