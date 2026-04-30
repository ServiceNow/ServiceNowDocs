---
title: Launch Onboarding modals
description: Configure programmatic triggers to launch Onboarding modals when to access specific pages or perform certain actions on their instance.
locale: en-US
release: zurich
product: Adoption Services
classification: adoption-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Onboarding modals launch]
breadcrumb: [Configure, Onboarding modals, Adoption services, Configure user experiences]
---

# Launch Onboarding modals

Configure programmatic triggers to launch Onboarding modals when to access specific pages or perform certain actions on their instance.

## Before you begin

Role required: admin

Ensure you have:

-   Created and published an Onboarding modals with at least one guidance step
-   Noted the sys\_id of your guidance record \(found in the URL when viewing the record\)
-   Identified the UI Builder page where the modal should launch
-   Access to UI Builder and the ability to create client scripts

## Procedure

1.  Launch UI Builder and navigate to the page where you want the modal to appear.

2.  In the left panel, select **Scripts** tab and create a new client script.

3.  In the script editor, enter the following code, replacing 'YOUR\_GUIDANCE\_SYS\_ID' with the actual sys\_id of your guidance record:

    ```
    api.emit('SN_HELP#GUIDANCE_START_REQUESTED', {guidanceId:'YOUR_GUIDANCE_SYS_ID'});
    ```

4.  Save the client script.

5.  In the left panel of UI Builder, select **Body**.

6.  In the right panel, select **Events** tab.

7.  Under Dispatched Events, select **Add**.

8.  In the **Event name** field, enter: `SN_HELP#GUIDANCE_START_REQUESTED`

9.  In the **Label** field, enter a descriptive name \(e.g., 'Onboarding Modal Launch'\).

10. Select **Save**.

11. Save and publish your UI Builder page.


## Result

The onboarding modal is configured to launch when users access the specified page. The modal will display the first guidance step and allow users to navigate through subsequent steps.

## What to do next

Test the modal launch by accessing the page as a user with the appropriate role assignment. Verify that all guidance steps display correctly and navigation options function as expected.

**Parent Topic:**[Configure](../concept/configure-onboarding-modals.md)

