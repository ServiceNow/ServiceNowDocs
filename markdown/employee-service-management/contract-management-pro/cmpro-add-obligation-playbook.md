---
title: Configure obligation review for the playbook
description: Create a page in UI Builder that uses a viewport component to dynamically load obligation review content in the playbook.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure the Playbook tab, Configure CM Pro for your workspace, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Configure obligation review for the playbook

Create a page in UI Builder that uses a viewport component to dynamically load obligation review content in the playbook.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Select the **Experiences** tab.

3.  Open your workspace.

4.  Create a new page by selecting the **+** icon.

    ![Add pages and variants on an experience page in UI Builder.](../image/cmpro-new-page-uib.png "Create page and variants")

5.  Select **Create from scratch instead**.

6.  On the form, enter the `Review Obligation List` in the **Name** field.

    The **URL path** will be automatically updated with `review-obligation-list`.

7.  Select **Looks good**.

8.  Complete the remaining steps to create the page.

    For more information, see Create a page in UI Builder.

9.  Add a viewport component for the page.

    For more information on adding a viewport, see Add a viewport component to your page.

    1.  In the configuration panel, select **+ Add** to attach the **Now Assist in Contract Management** page collection.

    2.  Select **Apply default configuration with added URL parameters** and then select done.

10. Create a client script for the page.

    For more information on adding a client script, see Define and bind client scripts to components.

    1.  Select **+** next to **Client scripts**.

    2.  Name your script.

        A descriptive name helps you know what the script does. It also makes it easier to find the script later when you add it to an event handler.

    3.  Add the following script.

        ```
        function handler({api, event, helpers, imports}) {
        
        api.emit("MACROPONENT_VIEWPORT_LOAD_REQUESTED", {
        
        viewportElementId: 'viewport_1',
        
        route: 'review-obligations',
        
        fields: {
        
        'cntrSysId': api.context.props.sysId,
        
        'diTaskSysId': api.context.props.diTaskSysId
        
        },
        
        params: {}
        
        });
        
        }
        ```

    4.  Select **Apply**.

11. Select the **Body** component and then select the **Events** tab under **Page configuration**.

    ![Events tab under Page Configuration.](../image/cmpro-page-events-tab.png "Events tab for page")

    1.  Select **Add handler** under the **Page ready** section.

    2.  Select the client script created in step 10.

    3.  Select **Continue**.

    The client script is bound to the Page ready event. When the page loads, this event handler automatically executes the client script.

12. If **Form Controller** is available under Data resources, remove it.

13. Navigate to the **General** tab under **Settings** and verify that **table**, **sysId**, and **diTaskSysId** are available under the **Required parameters**.

    If the parameters are not available, add them manually. For more information on modifying the page settings, see Edit page variant settings.


**Parent Topic:**[Configuring the Playbook tab on contract repository records](cmpro-config-playbook-tab.md)

