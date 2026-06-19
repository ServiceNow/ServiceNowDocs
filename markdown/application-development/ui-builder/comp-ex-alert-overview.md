---
title: Create and customize alert messages in UI Builder
description: Learn how alert messages help you communicate feedback and status updates using both default and scripted approaches.Add and configure alert messages for simple notifications without scripting.Use a client script to create dynamic, context-sensitive alert messages.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/ui-builder/comp-ex-alert-overview.html
release: australia
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [UI Builder, Alert, Alert message, Components, Use case, UI Builder, Alert, Alert message, Components, Use case, UI Builder, Alert, Alert message, Components, Use case]
breadcrumb: [Learn components by example, Customize UI Builder pages using components, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Create and customize alert messages in UI Builder

Learn how alert messages help you communicate feedback and status updates using both default and scripted approaches.

Alerts are components that display standardized notifications, such as feedback, warnings, and confirmations. They’re easy to configure without scripting, but you can add a script for more advanced functionality.

\[Omitted image "comp-ex-alerts-types.png"\] Alt text: A series of different types of alerts.

UI Builder supports several types of alert messages. To see how each one behaves, open the [Alert component documentation](https://horizon.servicenow.com/workspace/components/now-alert?release=zurich#overview) and try out different settings in the interactive preview.

**Parent Topic:**[Learn components by example](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/learning-components-by-example.md)

## Create alert messages in UI Builder

Add and configure alert messages for simple notifications without scripting.

### Before you begin

Role required: ui\_builder\_admin

### About this task

Use the default alert message configuration for simple notifications. In this example, the alert displays a personalized greeting using the logged-in user's full name.

This procedure uses UI Builder components to create dynamic, interactive layouts. For more information on how to configure components, see:

-   [Add and configure components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/add-components.md)
-   [UI Builder Quick Bits: Navigating Component Configuration](https://www.servicenow.com/community/next-experience-blog/ui-builder-quick-bits-navigating-component-configuration/ba-p/3181624)

<table id="table_exc_zzf_dhc"><thead><tr><th>

Component

</th><th>

Documentation links

</th></tr></thead><tbody><tr><td>

Alert

</td><td>

-   [Usage Guidelines](https://horizon.servicenow.com/workspace/components/now-alert?release=zurich)
-   [UIB Setup](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/now-alert/uib-setup%23properties)

</td></tr></tbody>
</table>Create and customize alert messages in UI Builder 

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/work-experiences.md) for more information on creating experiences.

3.  Create a page from scratch.

    For more information about how to create a page, see [Create a page in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/create-page.md).

4.  Add an alert.

    1.  In the content tree, select **+ Add content**.

    2.  Search for `alert` and then select **Add** to place the component on your page.

    3.  In the content tree, hover over **Alert 1** and select the configure icon \[Omitted image "uib-configure-icon.png"\] Alt text:, then select **Rename**.

        \[Omitted image "comp-ex-cam-rename.png"\] Alt text: Additional actions menu in the content tree open for the alert component, with a cursor hovering over the Rename option.

    4.  Replace the text in the **Component label** field with `Welcome Message`.

        The **Component ID** field auto-populates.

    5.  Select **Apply.**

5.  Configure the alert message.

    1.  With **Welcome Message** selected in the content tree, navigate to the configuration panel and set the following properties:

        |Field|Value or Action|
        |-----|---------------|
        |Type|**Info**|
        |Icon|**circle-info-outline**|
        |Header|**Heads up!**|
        |Link|\(Leave blank\) — select **Edit**, then delete any text inside **Label** and **Href**|
        |Action|\(Leave blank\) — select **Edit**, set **Type** to **-- None --**, then delete any text inside **Label** and **Href**|

        Your configuration panel should look like this:

        \[Omitted image "comp-ex-cam-config.png"\] Alt text: Configuration panel for alert, with highlights over the component label, Type, Icon, Header, Link, and Action fields.

    2.  Hover over the **Message** field and select the bind data icon \[Omitted image "uib-dynamic-data-binding-button.png"\] Alt text:.

    3.  Select **Formulas**, then **String**, then double-click or drag **CONCAT** to move the formula to the area above.

        \[Omitted image "comp-ex-cam-bind-data.png"\] Alt text: Bind data dialog showing CONCAT function with empty values.

    4.  Double-click **value1** to select the field, then select again to insert text.

    5.  Enter `"You're loggeded in as "`, making sure to include a trailing space after the exclamation point.

    6.  Double-click **values** to select the field, then select again to insert text.

    7.  Select **Data types**, then **Page properties**.

    8.  Under **Pill view**, select the pills in the following order: **session** &gt; **user** &gt; **fullName**.

    9.  Double-click or drag **fullName** to move it to the area above, then select **Apply**.

        \[Omitted image "comp-ex-cam-bind-data2.png"\] Alt text: Bind data dialog showing CONCAT function with "Welcome! " and @context.session.user.fullName as its values.

6.  Save and test your page.

    1.  Select **Save** in the upper-right.

    2.  Select **Preview**.

    The alert appears at the top of the page with the text "Heads up! You're logged in as " followed by the logged-in user's name.

    \[Omitted image "comp-ex-cam-alert.png"\] Alt text: Alert appearing under the header menu, greeting the logged-in user.


## Customize alert messages with a client script in UI Builder

Use a client script to create dynamic, context-sensitive alert messages.

### Before you begin

Role required: admin

### About this task

Scripted alerts provide notifications that respond to events or external data. They are highly flexible and can react to complex conditions, but require scripting knowledge and more effort to maintain. In this example, a button triggers a client script that generates multiple alerts with custom messages.

This procedure uses UI Builder components to create dynamic, interactive layouts. For more information on how to configure components, see:

-   [Add and configure components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/add-components.md)
-   [UI Builder Quick Bits: Navigating Component Configuration](https://www.servicenow.com/community/next-experience-blog/ui-builder-quick-bits-navigating-component-configuration/ba-p/3181624)

<table id="table_exc_zzf_dhc"><thead><tr><th>

Component

</th><th>

Documentation links

</th></tr></thead><tbody><tr><td>

Button

</td><td>

-   [Usage Guidelines](https://horizon.servicenow.com/workspace/components/now-button?release=zurich)
-   [UIB Setup](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/now-button/uib-setup%23properties)

</td></tr><tr><td>

Alert

</td><td>

-   [Usage Guidelines](https://horizon.servicenow.com/workspace/components/now-alert?release=zurich)
-   [UIB Setup](https://developer.servicenow.com/dev.do#!/reference/next-experience/zurich/now-components/now-alert/uib-setup%23properties)

</td></tr></tbody>
</table>Create and customize alerts in UI Builder 

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/work-experiences.md) for more information on creating experiences.

3.  Create a page from scratch.

    For more information about how to create a page, see [Create a page in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder/create-page.md).

4.  Add a button.

    1.  In the content tree, select **+ Add content**.

    2.  Search for `button` and add it from the toolbox.

    3.  In the content tree, hover over **Button 1** and select the configure icon \[Omitted image "uib-configure-icon.png"\] Alt text:, then select **Rename**.

    4.  Replace the text in the **Component label** field with `Showcase Alerts`.

        The **Component ID** field auto-populates.

    5.  Select **Apply**.

5.  Create a client script.

    1.  Under **Data and scripts**, select the **+** next to **Client scripts**.

        \[Omitted image "comp-ex-cam2-client-scripts.png"\] Alt text: Data and Scripts drawer with a highlight over Client scripts.

    2.  Replace the text in **Script name** with `Alerts`.

    3.  Replace the code with the following:

        **Tip:** You can select the format code icon \[Omitted image "comp-ex-dfc-format-code-icon.png"\] Alt text: to make the code more readable.

        ```
        /**
        * @param {params} params
        * @param {api} params.api
        * @param {any} params.event
        * @param {any} params.imports
        * @param {ApiHelpers} params.helpers
        */
        function handler({
            api,
            event,
            helpers,
            imports
        }) {
            api.emit("NOW_UXF_PAGE#ADD_NOTIFICATIONS", {
                items: [
                    {
                        id: "alert1",
                        status: "critical",
                        icon: "circle-exclamation-fill",
                        content: {
                            type: "html",
                            value: "<h2>Critical: System failure detected!</h2>"                   
                        },
                        action: { type: "dismiss" }
                    },
                    {
                        id: "alert2",
                        status: "high",
                        icon: "circle-exclamation-outline",
                        content: {
                            type: "string",
                            value: "High: CPU usage exceeded 90%"
                        },
                        action: { type: "dismiss" }
                    },
                    {
                        id: "alert3",
                        status: "moderate",
                        icon: "circle-pause-outline",
                        content: {
                            type: "string",
                            value: "Moderate: Disk space is below 20%"
                        },
                        action: { type: "dismiss" }
                    },
                    {
                        id: "alert4",
                        status: "warning",
                        icon: "triangle-exclamation-outline",
                        content: {
                            type: "html",
                            value: "<h4> Warning: A new software update is ready. </h4>"
                        },
                        action: { type: "dismiss" }
                    },
                    {
                        id: "alert5",
                        status: "info",
                        icon: "circle-question-fill",
                        content: {
                            type: "string",
                            value: "Info: A new software update is available"
                        },
                        action: { type: "dismiss" }
                    },
                    {
                        id: "alert6",
                        status: "positive",
                        icon: "check-circle-outline",
                        content: {
                            type: "string",
                            value: "Positive: Backup completed successfully"
                        },
                        action: { type: "dismiss" }
                    },
                    {
                        id: "alert7",
                        status: "low",
                        icon: "bell-fill",
                        content: {
                            type: "string",
                            value: "Low: Minor update recommended"
                        },
                        action: { type: "dismiss" }
                    }
                ]
            });
        }
        
        ```

    4.  Select **Apply**.

6.  Link the button to the client script with an event.

    1.  In the content tree, select the button we created: **Showcase Alerts**.

    2.  In the configuration panel, select the **Events** tab.

    3.  Under the **Button clicked** event, select **Add handler**.

    4.  Search for `alerts`, then select the **Alerts** handler under **Client Scripts**.

        \[Omitted image "comp-ex-cam2-events.png"\] Alt text: Events dialog showing the handler for the Alerts client script selected.

    5.  Select **Continue**.

    6.  Select **Add**.

7.  Save and test your page.

    1.  Select **Save** in the upper-right.

    2.  Select **Preview**.

    Selecting the button displays multiple alerts with messages that you define in the client script.

    \[Omitted image "comp-ex-cam2-alerts.png"\] Alt text: UI Builder editor showing a button and a series of custom scripted alerts.


