---
title: Create an investigation canvas
description: Create a new canvas to add observables from threat intelligence library.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2024-10-30"
reading_time_minutes: 2
breadcrumb: [Working with Investigation Canvases, Threat Analyst Workbench, Use, Threat Intelligence Security Center, Security Operations]
---

# Create an investigation canvas

Create a new canvas to add observables from threat intelligence library.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click the **Threat Analyst Workbench** icon.

3.  Go to **Investigation Canvases** &gt; **All Canvases**.

4.  Click **New**.

5.  Fill in the fields as appropriate.

    |Field|Description|
    |-----|-----------|
    |Name|Enter the name of canvas.|
    |Description|Add the description of the canvas.|
    |Linked Case|Option that displays the list of cases that do not have any canvases associated. This field value is populated based on the case that is linked to the corresponding canvas.|
    |Priority|Select the priority of the canvas.|
    |State|Select the state of the canvas.|

6.  Click **Save**

    The two new sections are displayed **Artifacts** and **Investigation Canvas**. When you create a new canvas, the canvas does not include any nodes. You must add nodes from Threat Intelligence library or artifacts through the option of add from library.

7.  Go to **Investigation Canvas**.

8.  Click **Add from Library**.

    **Note:** There are two options available to add the nodes. You can select either **Import** to import all the observables or select **Add from Library** option to add the observables from the threat intelligence library.

    The **Import node from Library** dialogue box displays.

9.  Select the **Type of node** from the drop down list.

    For example, select the type as Observables if you are adding observables to the investigation canvas.

10. Select the required number of observables.

11. Click **Import**.

    After you import observables, the nodes are added to the investigation canvas. Whatever the nodes that are added to the canvas are currently added temporarily to the canvas and it will not be persisted to the canvas.

12. Select **Save Canvas**.

    If you want to process the nodes data to the canvas then you must save the data to keep it permanently.

    **Note:** If you do not perform the **Save Canvas** option then you may loose the data whenever you refresh the canvas.

13. Select **Add Data to Library** to create any new relationship between two different nodes.

    The relationship between the two nodes is indicated with the dotted line which means the nodes are temporary. In case, if you want to move the nodes data to the relationships, then select **Save data to library** and add data to library. After you perform this operation the dotted line will turn to a solid edge line indicating that the node is now is part of the library.

14. Use the **Filter** icon to view the type of observables and objects that are present in the canvas and you can selectively choose the type of data to be shown under the investigation canvas.

15. Also, select the pop out icon to view or perform any operation on the investigation canvas nodes on a larger space.

16. Select **Link Case** to link the case to the investigation canvas.

    1.  Select the **Case ID**.

    2.  Click the **Link** button.

17. Click **Duplicate** to duplicate the canvas data and nodes within the canvas.


**Parent Topic:**[Working with Investigation Canvases](../concept/tisc-investigation-canvases.md)

