---
title: Define the payload for a custom modal
description: Set your action button to open a custom modal by defining the payload parameters.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure a custom form modal, Configure action buttons, Declarative actions, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Define the payload for a custom modal

Set your action button to open a custom modal by defining the payload parameters.

## Before you begin

-   [Create a form action](create-a-new-form-action.md)
-   [Activate Customer Service Management](https://www.servicenow.com/docs/access?context=t_ActivateCustomerService&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)
-   Open your record page in UIB or [create a page variant in UI Builder](https://www.servicenow.com/docs/access?context=create-variant&version=zurich&pubname=zurich-application-development&ft:locale=en-US)
-   [Customize your page variant in UI Builder](design-a-page-variant-in-uib.md#)
-   [Configure your page variant as a modal in UI Builder](configure-a-page-variant-as-a-modal-in-uib.md#)
-   [Create a UX add-on event mapping](create-a-ux-add-on-event-mapping.md#)

Role required: admin

## Procedure

1.  In the navigation filter, navigate to **All** &gt; **Declarative Actions** &gt; **Form Actions**.

2.  Select the form action where you want to add the custom modal.

3.  Open the **Specify client action** field by selecting the record preview icon \(![record preview icon](../../../use/collaboration/image/IconInfoTab.png)\) and **Open Record**.

4.  Mark the location of your page by entering the page's action name as the route key of the **Payload** field.

5.  Pass variables from the current context by entering the table and sysID values in the **fields** key.

    ```
     {
       "route": "action-name",
       "fields": {
         "table": "{{table}}",
         "sysId": "{{sysId}}"
       }
     }
    ```

6.  Select **Update**.

7.  Open a record in your configurable workspace.

8.  Test your button by selecting it.

    Your button opens the custom modal.


