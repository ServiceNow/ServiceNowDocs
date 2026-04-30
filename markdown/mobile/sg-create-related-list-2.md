---
title: Create a list screen to use as a related list
description: Create a related list using your parametrized data item. This list appears for your users when they select the related list tab on their form screen.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure a related list screen for a record screen, Record screen, Mobile screen types, Mobile screens, Mobile app components, Building mobile apps, Mobile Platform]
---

# Create a list screen to use as a related list

Create a related list using your parametrized data item. This list appears for your users when they select the related list tab on their form screen.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    The Mobile App Builder appears in a new browser tab and displays the application scope selection screen.

2.  Search for the application scope you're working in and then select the name of the application scope.

    The Mobile App Builder categories home screen displays.

3.  From the menu on the left side, select **Screens** to display the data items for the scope.

4.  Click the **New** button.

5.  Choose the **List** card from the **Create a screen** window.

6.  Use the **Properties** section to give your list a name and description.

7.  Select an icon by clicking the **Choose** button in the **Icon** section.

8.  Click the **Save** button in the upper right corner to save the list screen.

9.  In the **Screen segments** section, click **New** to create a section.

    A new **New screen segment** panel displays.

10. In the **Streams** section, click **New** to create a stream.

    A new **New list stream** panel displays.

11. In the **Data item** section, click **Choose**, and select the parametrized data item you created in [Create a parametrized data item for your related list](sg-create-related-list.md).

12. Return to the list screen record by selecting it in the configuration tree.

    This record should be the top level item on your configuration tree.![Mobile app builder configuration tree with screen highlighted](../image/mab-config-tree-1.png)

13. In the **UI Parameters** section, click **New**.

    Creating a UI parameter creates a link between the data item and the list screen.

14. In the **New UI parameter** screen, create a name and description for your parameter.

    Leave the remaining fields at their default values.

15. In the **Screen data parameter mapping** section, click the **Choose** button.

16. Find and select the data parameter from your data item.

    If you need to remember the name of this parameter, you can see it in the **Parameters** section of your data item record.

17. Click **Save** to save your list record.


## Example

Continuing the preceding example, you create an list screen to display incidents for your problem record. This list screen uses the data item created in the previous steps. This list screen needs a parameter to contain the problem record from your problem record screen. To make it easy to identify, the parameter name is also named `Problem`. In the IU Parameter Mapping section, you create a mapping between the data item parameter and the screen parameter, so the value can pass between them.

