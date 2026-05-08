---
title: Design a page variant in UIB
description: Configure a UI Builder page variant to pass from a workspace modal into the variant. This step acts as part of the process to configure an action button to open a custom modal.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure a custom form modal, Configure action buttons, Declarative actions, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Design a page variant in UIB

Configure a UI Builder page variant to pass from a workspace modal into the variant. This step acts as part of the process to configure an action button to open a custom modal.

## Before you begin

Complete the following actions:

-   [Create a form action](create-a-new-form-action.md)
-   Open your record page in UIB or create a page variant in UIB

Role required: admin

## Procedure

1.  Open a page variant in UI Builder.

2.  Add components to display on the page by selecting **+Add component** under the Body element.

3.  Select the added component and select the **Table** field.

4.  Switch the setting to **Bind data** and dot-walk to the table prop by entering `@context.props.table`.

5.  Select the **Title** field, and switch to **Script** mode.

6.  Enter the following script and pass the sysID received through the URL parameter as a JS template variable.

    ```
    function evaluateProperty({ api, helpers }) {
    	return `Only ${api.context.props.sysId}`;
    }
    ```

7.  Select **Apply** for the script and select **Save**.


## Result

The table and sysID variables are configured to be passed from the modal through the URL into the variant.

