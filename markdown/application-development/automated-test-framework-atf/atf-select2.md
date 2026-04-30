---
title: Select2 functionalities in ATF
description: Use the Select2 component to search and select your option from a drop-down menu easily.
locale: en-US
release: xanadu
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Custom UI test steps, UI test steps, Building and running automated tests with the Automated Test Framework, Test your apps with the ATF, Testing and debugging applications, Building applications]
---

# Select2 functionalities in ATF

Use the Select2 component to search and select your option from a drop-down menu easily.

You can set the value of select2 in a test. The test then searches for the value in the search bar of Select2. The first valid result in the component drop-down gets selected.

Drag and drop the page inspector on the required drop-down menu. The right panel for the selected component opens. You can specify the text you want to search in the set component value step within the page inspector.

Select the **Set Component Value** option under **Action** to search for a component. Type in the text in the right panel and click **Submit**. This enables the code to open the select2 to search for that component and pick the first option that shows up.

**Note:** If multiple, similarly named component options show up on searching a term, only the first option is selected.

![Gif showing the select2 functionalities](../image/select2.gif "Select2 component")

## Limitations of the select2 support

-   Only certain versions \(3.5.1-3.5.4 and 4.0.0-4.0.13\) of the select2 library are supported.
-   The select2 support depends on the jquery library. So, if you try to set a value of select2 and the name of the jquery library is changed, it causes the test to fail.
-   Searching through Select2 won’t work when there is no search bar.

## Design considerations

Search and select your options efficiently with the following design considerations:

-   It is recommended to use uniquely searchable test data
-   Wait for the current element to be set before proceeding to set the next element while setting the value of Select2 via the Set Component Values \(Custom UI\) test step
-   Prevent failing of tests by avoiding jquery library name change
-   Select2 Adapter and Decorator features are not supported

**Parent Topic:**[Custom UI test steps](custom-ui-test-steps.md)

