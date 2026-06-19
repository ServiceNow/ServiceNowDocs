---
title: Define the payload for a custom modal
description: Set your action button to open a custom modal by defining the payload parameters.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/configure-user-experiences/define-the-payload-for-a-custom-modal.html
release: australia
product: Configure User Experiences
classification: configure-user-experiences
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure a custom form modal, Configure action buttons, Declarative actions, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Define the payload for a custom modal

Set your action button to open a custom modal by defining the payload parameters.

## Before you begin

-   [Create a form action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/create-a-new-form-action.md)
-   Open your record page in UIB or create a page variant in UIB
-   [Design your page variant in UIB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/design-a-page-variant-in-uib.md)
-   [Configure your page variant as a modal in UIB](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/configure-a-page-variant-as-a-modal-in-uib.md)
-   [Create a UX add-on event mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-user-experiences/create-a-ux-add-on-event-mapping.md)

Role required: admin

## Procedure

1.  In the navigation filter, navigate to **All** &gt; **Declarative Actions** &gt; **Form Actions**.

2.  Select the form action where you want to add the custom modal.

3.  Open the **Specify client action** field by selecting the record preview icon \(\[Omitted image "IconInfoTab.png"\] Alt text: record preview icon\) and **Open Record**.

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


