---
title: Import queues
description: Import queues from your contact center provider to ensure that customer interactions are routed to the appropriate agents based on their skills and availability.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [CCaaS Admin Console, Integrating with contact centers, Integrate, Customer Service Management]
---

# Import queues

Import queues from your contact center provider to ensure that customer interactions are routed to the appropriate agents based on their skills and availability.

Role required: admin \(sn\_ct\_ctr\_it\_core\)

Follow these steps in the workflow to import queues from your selected contact center:

-   **Step 1: Select queues**

    Identify the queues that you want to import from your selected contact center provider.

-   **Step 2: Assign channels**

    Select queues, assign service channels to them, and import them into ServiceNow.

-   **Step 3: View summary**

    Review the newly imported queues and the ones that existed before in your ServiceNow instance.


**Note:** The **Start Over** button resets your current changes and takes you back to the **Select queues** step.

## Select queues

1.  Navigate to **All** &gt; **Contact Center Integration Center** &gt; **Contact Center Admin Console**.
2.  Select a contact center provider to import queues from the dropdown menu for the **Select a provider** field.

    **Note:** The contact center dropdown menu appears only when multiple providers are configured. If you have just one provider, it's automatically selected and can't be changed.

3.  Select the **Import Queues** tab from the navigation pane.

    ![ISelect queues from your selected contact center provider for importing](../image/int-import-queues-select-queues.png "Select queues for importing")

4.  Search for specific queues by using the search bar or select **Fetch all queues** to fetch the entire list of available queues.
5.  Once you’ve fetched a set of queues, select the queues you plan to import by selecting the check box next to each queue.

    **Note:** You can also select all queues by selecting the check box at the top of the list.

6.  Select each queue that you want to import and click **Continue**.
7.  Proceed to the next step of assigning service channels for your selected queues.

## Assign channels

![Select queues and assign service channels](../image/int-select-queues-to-assign-service-channels.png "Select queues to assign service channels")

1.  Select one or more queues from the displayed queues list by selecting the check box next to them.

    **Note:** You can select all queues by selecting the check box at the top of the queues-list.

2.  Select **Assign service channels** to display the service channel modal.

    ![Assign service channels for selected queues](../image/int-assign-service-channels.png "Assign service channels")

3.  Select one or multiple service channels and assign them to the selected queues.
4.  Repeat steps \(1\) through \(3\) and confirm that all queues have at least one service channel assigned to them.
5.  Select **Import** to begin the import process.

    **Note:** Each pairing of a new queue and service channel creates a unique queue record in ServiceNow.

    ![Import queues with assigned service channels](../image/int-import-queues.png "Import queues")


## View summary

![View summary of new and existing imported queues from the contact center provider](../image/int-view-summary.png "Summary of import")

1.  In the **View summary** step, review a summary of your recent actions.
2.  Additionally, you can also choose to import more queues or view all queues in the table.
3.  Review the list of queues to confirm their successful import.
4.  The new imported queues and queues that previously existed are displayed in two separate lists in the confirmation page.

## Example: Fetch all queues, assign a service channel, and import all queues

The following example demonstrates how to fetch all available queues, assign the Chat service channel, and import them into ServiceNow.

1.  Select **Fetch All** to retrieve all queues from the CCaaS provider.
2.  Select all queues using the **Name** field or **Select all item\(s\)** link.
3.  Select **Import** to proceed to the channel assignment step.
4.  Repeat step \(2\).
5.  Select **Assign service channels**, then select Chat, and select **Assign**.
6.  The refreshed screen shows all queues with the Chat service channel assigned.
7.  A banner confirms the successful assignment.
8.  Select **Import** to start the import process.
9.  Review a summary of your import in the **View summary** step.

