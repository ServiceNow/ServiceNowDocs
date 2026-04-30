---
title: Create a Work scheduler card using the Next Experience UI Builder
description: Create a work scheduler card and add the components that you want to display based on your needs in the Work Scheduler application in manager workspace.
locale: en-US
release: xanadu
product: Workforce Optimization for IT Service Management
classification: workforce-optimization-for-it-service-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Setting up Work scheduler in Workforce Optimization for ITSM, Work scheduler in Workforce Optimization for ITSM, Workforce Optimization for ITSM, IT Service Management]
---

# Create a Work scheduler card using the Next Experience UI Builder

Create a work scheduler card and add the components that you want to display based on your needs in the Work Scheduler application in manager workspace.

## Before you begin

Role required: admin, workspace\_admin, or ui\_builder\_admin​

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  In the **My experiences** list, select **Manager Workspace**.

3.  Select the Pages icon.

4.  In the **Page** menu, select **Work scheduler**.

5.  In the left pane, go to the **Content** section and navigate to **Body \(Flex\)** &gt; **Work queue \(Flex\)** &gt; **Sidebar**.

6.  In the right pane, select the icon \(![Edit card icon](../image/edit-card-icon.png)\) in the **Work item cards default** sub-page.

7.  In the left pane, select **Body \(Flex\)** &gt; **Viewport1**.

8.  In the right pane, select **+Add** and enter a name for the card.

    The **Path** field is automatically populated.

9.  Select **Create**.

    A new card is created.

    **Important:** After you create the work scheduler card, you must select the name of this card in the **UX app route** field in the work configuration you have created. For information on setting up a work configuration, see [Set up a work configuration](setup-work-scheduler.md).

10. Select **Done**.

    Follow the steps listed in each of the topics below in the given sequence to customize Work scheduler.


1.  [Create a client state parameter for Work scheduler](work-sched-create-client-state-params.md)  
Add custom client state parameter values to add properties to the card components.
2.  [Create page scripts for Work scheduler](work-sched-create-page-scripts.md)  
Add custom page scripts for the Work scheduler so that you can update the client state through events or update transform workItem object to properties.
3.  [Define the workItem property in the Work scheduler page configuration](work-sched-create-page-properties.md)  
Add the **workItem** property to the Work scheduler page configuration to receive the **workItem** object provided by the work queue.
4.  [Define event mappings for Work scheduler](work-sched-event-mapping.md)  
Add event mappings required for card interactions and for the card properties transformation to the page configurations in Work scheduler.
5.  [Configure container components for Work scheduler](work-sched-card-based-container.md)  
Present information in an intuitive format using the Card Base Container component.
6.  [Configure a Work scheduler card heading component](work-sched-card-based-header.md)  
Customize the Work scheduler heading component to display the title based on your needs.
7.  [Configure a display type component for a Work scheduler card](work-sched-stacked-component.md)  
Add the **Label value stacked** display work item fields within the card.
8.  [Configure an avatar component for Work scheduler](work-sched-avatar-component.md)  
Use the **Container** component to add an avatar and the user name of the work item assignee.
9.  [Associate a work scheduler card to the work configuration](associate-card-config-wfo-itsm.md)  
Associate the work scheduler card that you've created to the work configuration to display the card in the Work scheduler sidebar.

**Parent Topic:**[Setting up Work scheduler in Workforce Optimization for ITSM](../concept/setting-up-work-scheduler.md)

**Related topics**  


[Create a page in UI Builder](https://www.servicenow.com/docs/access?context=create-page&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)

