---
title: Create a Now Experience Framework page in UI Builder
description: To configure mobile web screens that use Mobile App Bridge to leverage a playbook on mobile devices, the first step is to create a Now Experience Framework page in UI Builder.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Configure mobile web screens with Mobile App Bridge, Mobile App Bridge, Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Create a Now Experience Framework page in UI Builder

To configure mobile web screens that use Mobile App Bridge to leverage a playbook on mobile devices, the first step is to create a Now Experience Framework page in UI Builder.

## Before you begin

Role required: admin

## About this task

You must create a Now Experience Framework page in [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) before you can configure mobile web screens that can leverage a playbook on mobile devices. After you configure the page, you must configure a web screen in Mobile App Builder \(MAB\). For details about configuring mobile web screens that use Mobile App Bridge to leverage platform features on mobile devices, see [Configure mobile web screens with Mobile App Bridge](configure-mobile-playbooks.md).

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  In the UI Builder Home page, select **Create** on the upper right.

3.  Complete the **Create an experience** dialog box and select **Create** when you're finished.

    ![UI Builder dialog box where you can name your Now Experience Framework page, specify roles for it, and specify the App shell UI.](../image/mob-playbk-select-app-shell-ui.png)

    **Note:** Select **UXR Base Experience Shell** from the **App shell UI** drop-down list.

4.  Select **Open experience** and then select **Create a new page**.

5.  Select **Create from scratch instead**.

    For information about working with templates or creating a page from scratch in UI Builder, see [Customize the Playbook Experience](https://www.servicenow.com/docs/access?context=playbook-customize-playbook&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

6.  Name the page and select **Continue**.

7.  Review the URL parameters and if they’re what you want, select **Looks good**.

8.  Configure the page variant name and audience or accept **Default**, add **Conditions** if needed, and then select **Create**.

9.  In the page, select **Open in editor** in the upper right corner.

10. Select the data icon on the left side of the page to launch the Data resources dialog box, and then select **+Add**.

11. In the Search data resources dialog box **Applications** column, select **@servicenow/now-mobile-app-bridge**, and then in the **Data resources** column, select **Mobile app**.

    !['Search data resources' dialog box showing selection of @servicenow/now-mobile-app-bridge > Mobile app, and then selecting the Add button.](../image/mob-playbk-sel-mob-app-brdg.png)

12. In the lower right corner of the dialog box, select **Add** to add the Mobile App Bridge data resource to the page.

    **Note:** Scroll down the page to see the **Add** button if it isn't visible.

13. Add event handlers to trigger Mobile App Bridge APIs to enable native functionality on mobile screens.

    For example, if you want an event to be triggered for a button on the mobile device:

    1.  Select **Body** on the left side of the editor page, and then select **Add component**.

        ![UI Builder user interface showing how to add a component.](../image/mob-playbk-add-button.png)

    2.  Select the **Components** tab and then select the type of button you want to use.
    3.  Select the button component you just added in the body of the page, select the **Events** tab in the dialog box on the right, and then select **Add event handler**.

        ![UI Builder user interface showing how to select the option to 'Configure the component manually.'](../image/mob-playbk-config-comp-man.png)

    4.  In the **Select event handler below…** dialog box, select one of the event handlers under **Mobile app 1**, and then configure it.

        **Note:** Be sure to enter the `sysid` of a valid mobile screen in the **Screen ID** field:

        ![UI Builder user interface showing where to add the mobile screen sysid in the 'Screen ID' field.](../image/mob-playbk-add-sysid4mobapp.png)

    5.  When you've finished configuring the event handler, select **Add** in the lower right corner of the dialog box.
14. In the Now Experience Framework editor page, select **Save** in the upper right corner to save the page.

    For information about configuring a playbook, see [Customize the Playbook Experience](https://www.servicenow.com/docs/access?context=playbook-customize-playbook&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

    **Note:** The getTitle\(\) method in the GlideListProperties API isn't available in Mobile App Bridge to configure Next Experience \(Seismic\) pages.


## What to do next

After you’ve created the Now Experience Framework page, you must create a mobile web screen in MAB. Then you must add the Now Experience Framework page URL to the mobile web screen configuration in MAB. For details on completing this configuration, see Step 2 in [Configure mobile web screens with Mobile App Bridge](configure-mobile-playbooks.md).

**Parent Topic:**[Configure mobile web screens with Mobile App Bridge](configure-mobile-playbooks.md)

