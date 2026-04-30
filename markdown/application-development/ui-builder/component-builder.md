---
title: Create custom components to reuse across pages with component builder
description: Reuse custom components across experiences and pages in UI Builder.Build reusable custom components to use across experiences and pages in UI Builder.
locale: en-US
release: zurich
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 11
breadcrumb: [Component Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Create custom components to reuse across pages with component builder

Reuse custom components across experiences and pages in UI Builder.

Create custom components in UI Builder's component building UI. The component building UI shares many similarities to page building and enables you to configure components the same way you would when configuring a page in UI Builder.

## The power of custom components

Building custom components improves efficiency, consistency, and maintainability across your experience. By creating reusable UI elements, you avoid duplicating configurations, ensure a uniform look and feel, and make it easier to manage updates or design changes. Custom components also simplify complex layouts, support flexible configurations, and enable for easier testing and debugging. They’re also helpful in team environments, where shared components help streamline collaboration and keep the user experience consistent at scale.

Custom components are especially valuable when designing pages for different user types within your experience. For example, you can create a reusable component that includes both a list and a data visualization, then tailor its content or behavior based on the user group enabling you to maintain a consistent layout while delivering role-specific information.

Components edited in the Component Builder will automatically update on all pages where they are used.

**Important:** Custom components created in an instance remain available only within that instance until they are migrated to other instances using update sets or application installations.

## Custom components or page collections

To build efficient, scalable digital experiences, it’s important to reuse elements wherever possible. Two ways to do this are through custom components and page collections. Each serves a distinct purpose depending on the scope of reuse that you need.

-   **Custom Components**

    Use custom components when you want to replicate a specific part of a page like a heading, list, form, or buttons across multiple pages.

    You want to apply a consistent theme or configuration to a component or group of components.

    You're designing pages to be modular or flexible where parts of a page may change but shared components remain consistent.

    You want to manage changes in one place and have them updated everywhere the component is used.

    Multiple teams are simultaneously working on different sections of the same page.

-   **Page Collections**

    You want to reuse an entire page layout and configuration across multiple pages or experiences.

    You must build a variation of full pages for different users or workflows.

    You want to use a set of tabs across multiple pages or experiences.


## Custom component UI

You can access the component builder in UI Builder by selecting **Create** in the header or the **Component** tile on the UI Builder home page.

![UI Builder homepage with arrows pointing the component create buttons.](../image/component-builder-create-buttons.png "UI Builder home page")

![Component builder homepage.](../image/component-builder-home.png "Component Builder UI")

Components built with UI Builder can be found in the toolbox when adding a component to a page and in the component list on the home page of UI Builder. You can update or modify custom components by locating it in the components list on the home page of UI Builder.

![The alt text modal displays when test values is selected.](../image/cb-test-values.png "Test Values in Component Builder")

Use test values in component builder to supply simulated values for required and optional URL parameters when building a custom component. Test values help validate how a component will act when added to a page by ensuring bindings and data resources are functioning correctly. For more information about test values see, [Test values in a page](test-value.md).

![UI Builder homepage displaying the components tab.](../image/components-list-home.png "Component List")

You can quickly duplicate a custom component from the component settings screen by selecting **Duplicate**, which creates an exact copy of the component for reuse or modification.

![Component settings screen with an arrow displaying the Duplicate option.](../image/custom-component-duplicate.png "Custom Component Settings")

## Component Builder vs NOW CLI Component Development

There are two ways to build components for UI Builder. The first is using the low-code component within UI Builder, which offers a drag-and-drop interface for creating custom components. The second is using [NOW CLI developer tools](https://developer.servicenow.com/dev.do#!/reference/next-experience/yokohama/cli/getting-started) to build components through code. Both methods produce components that can be added to the UIB toolbox and reused across experiences. Keep in mind that changes to included components may impact both types.

Although both tools create components for UI Builder, there are important differences to consider.

Component Builder in UI Builder:

-   Components built within UI Builder can reference controllers and data resources.
-   Creates "Macroponent Components," which are stored in the sys\_ux\_macroponent table.
-   Component Builder is ideal for users who prefer a visual, drag-and-drop interface for building components.
-   Great for quickly creating simple to moderately complex components.

NOW CLI components:

-   Intended for developers who need to write custom HTML, CSS, and JavaScript.
-   Suitable for building complex and customizable components.
-   Components created with NOW CLI are stored in the sys\_uib\_toolbox\_component table.

## Best practices

The UI Builder custom component builder lacks governance capabilities and can lead to duplication and inconsistency in your experience. Teams may create similar components with slight variations, resulting in a fragmented UI, and confusing user experience. It is recommended that your team completes regular audits and cross-team communication to maintain alignment and avoid fragmentation as your experiences grows.

All components are designed to be upgrade safe, as long as their security policy is set to `read_only`. This provides greater upgrade protection for larger components or page partials compared to other deployable units like bundles and page templates. However, this also means that out-of-the-box \(OOTB\) components may not be editable.

**Parent Topic:**[Component Builder](component-builder-uib.md)

## Create components to reuse across pages

Build reusable custom components to use across experiences and pages in UI Builder.

### Before you begin

Role required: ui\_builder\_admin

### About this task

In this Component Builder example, we will create a stopwatch component to track elapsed time, which can be added to any page. The component will include customizable properties that can be modified once it's placed onto a page.

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Select **Create** from the UI Builder home page.

    ![UI Builder home page with the Create component button.](../image/create-component-button.png)

3.  Select **Component**.

4.  In the form, fill in the fields.

    ![Create a component form.](../image/create-component-form.png "Create a component dialog box")

    |Field|Description|
    |-----|-----------|
    |Name|Add a name to track your component internally. The component name appears in the toolbox. For this example, it is `Stopwatch`.|
    |Categories|Add a category to your component to help easily find it in the toolbox. You can update the category later in the Settings. For this example select **Content**.|
    |Description|Add description to describe when and how to use your component.|
    |Icon|Select an icon to represent the component in the toolbox.|

5.  Select **Create**.

    The page opens in Component Builder view.

    ![Custom component building UI showing the content and configuration side bars.](../image/create-component-editor.png)

6.  Add a custom component property by selecting **+ Add property** in the **Properties and policy** section.

    ![Select Add property to add content](../image/cb-add-property.png)

    1.  Select **String** from the list.

    2.  Enter the following values in the configuration panel.

        |Field|Value|
        |-----|-----|
        |Property label|`SVG Image Source`|
        |Property ID|`svgImageSource`|
        |Default value|`animateddino.svg`|

        ![Custom component building UI with arrows pointing to the Property label, Property ID, and SVG Image Source fields in the configuration panel.](../image/cb-component-properties.png)

    3.  Select **Save**.

7.  Configure the layout for the custom component by selecting the **+ Add Content** button.

    1.  Select **Single column**, then select **Add**.

    2.  In the content tree, under **Column 1**, select **+Add content**.

    3.  Select **Card Base Container**, then select **Add**.

    4.  In the content tree, under **Card Base Container 1**, select **+ Add content**.

    5.  Select **Layouts**.

    6.  Select **Flexbox**, then select **Add**.

    7.  Select **Save**.

        ![Add content to a container](../image/cb-component-layout.png)

8.  Add a stylized text component in our Flexbox container by selecting **+ Add content** under **Container 1**.

    1.  Select the **Stylized text** component, then select **Add**.

    2.  Select **Cancel** to close the preset window.

    3.  Select **Save**.

        ![Add stylized text to a container](../image/cb-stylized-text-component.png)

9.  To configure the stylized text component we will add some client state parameters.

    1.  Select **Client state parameters** in the **Data and scripts** section.

    2.  In the **Edit client state parameters** dialog, enter the following values:

        |Name|Type|Initial value|
        |----|----|-------------|
        |startTime|Number| |
        |elapsedTime|String|00:00:00|
        |timeinterval|JSON| |
        |stopwatchRunning|Boolean| |
        |intervalId|String| |

    3.  Select **Apply**.

        ![List of client state parameters added to the custom component.](../image/cb-client-state-parameters.png)

    4.  Select **Save**.

10. To configure the stylized text component we are going to bind the **elapsedTime** client state parameter.

    1.  Select the **Stylized text 1** component in the content tree.

    2.  Select the bind icon when pointing to the **Text** field of the stylized text component.

        ![Bind stylized text in component](../image/cb-text-bind-icon.png)

    3.  Select **Client states**.

    4.  Double-click the **elapsedTime** pill.

        ![Bind the elapsed time parameter to text](../image/cb-elapsedtime-pill.png)

    5.  Select **Apply**.

    6.  Select **Save**.

11. Add a Flexbox container to hold the buttons.

    1.  Select the **+** icon under the stylized text component.

        ![Select the plus sign under the text component](../image/cb-add-component-icon.png)

    2.  Select **Layouts**.

    3.  Select **Flexbox**.

    4.  Select **Add**.

12. Add and configure the stopwatch running renderer and the start button.

    1.  Select **+ Add content** in the container you added in the previous step and add a **Conditional renderer**.

    2.  Select **+ Add condition** in the content tree.

    3.  Select **Single component**, then select **Next**.

    4.  Select **Button iconic**, then select **Next**.

    5.  In the **Edit settings** dialog, enter the following values:

        -   Component label: `Start`
        -   Component ID: `start_button`
        -   Render content: **Always**
    6.  Select **Apply**.

    7.  Select the **Start** button in the content tree.

    8.  Set the following properties in the configuration panel.

        |Field|Value|
        |-----|-----|
        |Icon|**stopwatch-fill**|
        |Variant|**Primary**|
        |Size|**Large**|
        |Tooltip text|`Start`|

    9.  Select **Save**.

        ![Custom component building UI with arrows pointing to the component label, and Icon, Variant, Size, and Tooltip text fields in the configuration panel.](../image/cb-add-renderer.png)

13. Configure the stop button to display while the stopwatch is running.

    1.  Select **+ Add condition** in the content tree.

    2.  Select **Empty container**, then select **Next**.

    3.  In the **Edit settings** dialog, enter the following values:

        -   Component label: `Running`
        -   Component ID: `running_container`
        -   Render content: **When condition below is true**
    4.  Select the bind icon while pointing at the **Condition** field.

        ![Edit settings modal where you select to bind](../image/cb-condition-bind-icon.png)

    5.  Select **Client states**, then double-click the **stopwatchRunning** pill.

    6.  Select **Apply**.

    7.  Select **Apply**.

    8.  Select **+ Add content** in the **Running** container and add a **Button iconic**.

    9.  Select **Button iconic 1** in the configuration panel and enter the following values:

        -   Component label: `Stop`
        -   Component ID: `stop_button`
    10. Select **Apply**.

    11. Set the following properties in the configuration panel.

        |Field|Value|
        |-----|-----|
        |Icon|**stopwatch-fill**|
        |Variant|**Secondary**|
        |Size|**Large**|
        |Tooltip text|`Stop`|

    12. Select **Save**.

        ![Custom component building UI with arrows pointing to the component label, and Icon, Variant, Size, and Tooltip text fields in the configuration panel.](../image/cb-add-renderer2.png)

14. Reorder the conditions so that **Running** appears above **Start**.

    1.  Select **Conditional renderer 1** in the content tree.

    2.  In the configuration panel, select and drag the drag handle icon ![](../image/drag-handle.png) to move the conditions into position.

        ![Conditional renderer component in the configuration panel with the "Running" condition placed near the "Start" condition.](../image/cb-reorder-conditions.png)

        Conditions are evaluated in order from top to bottom, so **Running** must appear above **Start** for the buttons to display correctly.

15. Add the logic for the component by selecting **+** next to **Client scripts** in the **Data and scripts** section.

    1.  Enter `Start` in the **Script name** field.

    2.  Paste the following script into the script field.

        ```
        function handler({ api, helpers }) {
          console.log('Start script running');
         
          if (api.state.stopwatchRunning === undefined) {
            api.setState('stopwatchRunning', false);
            api.setState('elapsedTime', '00:00:00');
            api.setState('startTime', null);
            api.setState('intervalId', null);
          }
         
          let running = api.state.stopwatchRunning;
         
          function pad(n) {
            return n < 10 ? '0' + n : n.toString();
          }
         
          function updateElapsedTime(startTime) {
            if (!running) {
              if (api.state.intervalId) {
                helpers.timing.clearInterval(api.state.intervalId);
                api.setState('intervalId', null);
                console.log('Interval cleared');
              }
              return;
            }
         
            if (!startTime) {
              console.log('No startTime passed to updateElapsedTime, cannot update');
              return;
            }
         
            const now = Date.now();
            const elapsedMs = now - startTime;
         
            const totalSeconds = Math.floor(elapsedMs / 1000);
            const hours = pad(Math.floor(totalSeconds / 3600));
            const minutes = pad(Math.floor((totalSeconds % 3600) / 60));
            const seconds = pad(totalSeconds % 60);
         
            const formattedTime = `${hours}:${minutes}:${seconds}`;
         
            console.log('Setting elapsedTime:', formattedTime);
            api.setState('elapsedTime', formattedTime);
          }
         
          if (!running) {
            const now = Date.now();
         
            api.setState('startTime', now);
            api.setState('elapsedTime', '00:00:00');
            api.setState('stopwatchRunning', true);
            running = true;
         
            if (api.state.intervalId) {
              helpers.timing.clearInterval(api.state.intervalId);
              api.setState('intervalId', null);
              console.log('Existing interval cleared before starting new one');
            }
         
            // Pass startTime directly here
            updateElapsedTime(now);
         
            const id = helpers.timing.setInterval(() => {
              updateElapsedTime(now);
            }, 1000);
            api.setState('intervalId', id);
            console.log('Interval started with id:', id);
          } else {
            if (!api.state.intervalId) {
              // Use existing startTime from state, but be mindful it might still lag
              const storedStartTime = api.state.startTime || Date.now();
              const id = helpers.timing.setInterval(() => {
                updateElapsedTime(storedStartTime);
              }, 1000);
              api.setState('intervalId', id);
              console.log('Interval restarted with id:', id);
            }
          }
        }
        ```

    3.  Select **Apply**.

        ![Edit client script modal overlaying the UI Builder editor.](../image/cb-add-client-script.png)

    4.  Select **+** next to **Client scripts** to add a second script.

    5.  Enter `Stop` in the **Script name** field.

    6.  Paste the following script into the script field.

        ```
        function handler({ api, helpers }) {
          console.log('Stop script running');
         
          if (api.state.stopwatchRunning === undefined) {
            // If state is not initialized yet, initialize it to avoid errors
            api.setState('stopwatchRunning', false);
            api.setState('elapsedTime', '00:00:00');
            api.setState('startTime', 0);
            api.setState('intervalId', null);
          }
         
          if (api.state.stopwatchRunning) {
            api.setState('stopwatchRunning', false);
            if (api.state.intervalId) {
              helpers.timing.clearInterval(api.state.intervalId);
              api.setState('intervalId', null);
            }
          }
        }
        ```

    7.  Select **Apply**.

    8.  Select **Save**.

16. Add event handlers to the buttons we created in the previous steps.

    1.  Select the **Start** button in the content tree and open the **Events** tab in the configuration panel.

    2.  Select **Add handler** under **Button iconic clicked**, then select the **Start** client script we created in the previous steps.

        ![Add event handler modal with an arrow pointing to a client script labeled "Start."](../image/cb-add-event.png)

    3.  Select **Continue**, then select **Add**.

    4.  Select the **Stop** button in the content tree and open the **Events** tab in the configuration panel.

    5.  Select **Add handler**, then select the **Stop** client script we created in the previous steps.

    6.  Select **Continue**, then select **Add**.

    7.  Select **Save**.

17. Select **Preview** to test the configured components.

    ![UI Builder preview of page with running stopwatch component.](../image/cb-preview.png)


### Result

Your custom component is now available in the UI Builder toolbox.

