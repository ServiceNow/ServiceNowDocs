---
title: Create a test for Configurable Workspace interaction via Page Inspector
description: Leverage the Page Inspector to create tests by directly interacting with components on most Configurable Workspace pages.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Testing Configurable Workspace components, Administering the Automated Test Framework \(ATF\), Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Create a test for Configurable Workspace interaction via Page Inspector

Leverage the Page Inspector to create tests by directly interacting with components on most Configurable Workspace pages.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Automated Test Framework \(ATF\)** &gt; **Tests**.

    A list of ATF tests shows up.

2.  Select **New** to create a new test.

3.  Fill up the fields and submit it.

4.  Select **Add Test Step** on the created test form.

5.  Select the Configurable Workspace test step category.

6.  Select Open Workspace Page test step.

    **Note:** This step is applicable if you want to navigate to a workspace page using a URL.

    1.  Fill up the details on the Open Workspace Page form.
    2.  Add the workspace URL you want to use in the Workspace URL field.
    3.  Select **Submit** to create the test step.
7.  Select **Add Test Step** on the created test form again and select the Configurable Workspace test step category.

    **Note:** This step is applicable only if you want to create another Configurable Workspace test step.

8.  Select Test Page test step.

    **Note:** This step is applicable only if you want to interact with a seismic component on a workspace page. See [Testable Configurable Workspace components](../reference/atf-conf-ws-components.md) for more information.

    The Configurable Workspace Test Authoring modal shows up.

    1.  Enter the URL of the workspace page you want to inspect.

        **Note:** By default, the URL selected in the Open Workspace Page test step shows up. If you haven't created an Open Workspace Page test step, you must enter the workspace URL you want to inspect.

    2.  Select **Open** to open the workspace page. The workspace page opens up in a new tab. You will notice a right panel that displays the components of the page you want to inspect.
    3.  Select REFRESH COMPONENT LIST to make sure it shows all the components on the page.
    4.  Drag and drop the inspector on a component on the page.

        **Note:** The name of the selected component is displayed on the right panel. Along with that, actions related to the selected component are also displayed. Select the required action for the component. These actions are actions that are understood by the components.

    5.  Select the required action for the component.
    6.  Enter the value for any inputs and optionally enter an expected return value to assert for the selected action.
    7.  Select **Submit** to create the test step.
9.  Continue adding Test Page steps until all required navigation and component interaction is accomplished.

    Test steps can be viewed, deleted, or reordered in the dropdown under the test name or by reloading the Test Steps related list on the test form.

    **Note:** The Test Steps related list information on the test form get updated with the previous steps.

10. Open a Test Page test step from the test form related list and select **Edit page interaction** to modify existing Test Page steps or resume a test authoring session.

    The Page Inspector loads the workspace page from the most recent Open Workspace Page step and replay all Test Page steps in the batch. Deleting previous steps results in the reload and replay of all Test Page steps in the batch to validate a successful workspace navigation path.


**Parent Topic:**[Testing Configurable Workspace components](../concept/atf-conf-ws.md)

