---
title: Synchronize Indoor Mapping map data with CMN location
description: Synchronize the CMN Locations and Location place types with Indoor Mapping map data, places, and place types.
locale: en-US
release: australia
product: Indoor Mapping
classification: indoor-mapping
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Synchronize Indoor Mapping with CMN Locations, Manage map objects and data, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Synchronize Indoor Mapping map data with CMN location

Synchronize the CMN Locations and Location place types with Indoor Mapping map data, places, and place types.

## Before you begin

Role required: admin

## Procedure

1.  Make sure that you have configured Indoor Mapping locations, floor plan, and map object:

    -   Add campus, building, and floors in Map studio. For more information, see [Create a campus with buildings and floors](create-a-campus-building-and-floor.md).
    -   Add floor plan to a floor. For more information, see and [Manage CAD source files](../concept/manage-autocad-files.md).
    -   Add places in Map studio. For more information, see [Manage places](manage-buildings.md)
    -   Enable the Default view in the Indoor Mapping Map studio. In the Indoor Mapping select **View editor** &gt; **Default**. Select **All content**.

        **Note:** Enabling the default view in Indoor Mapping is a mandatory step. The Default view is required to render the floor maps in Workplace Service Delivery. For more information, see [Edit with view editor](edit-with-view-editor.md).

2.  Navigate to **Indoor Mapping** &gt; **Campuses**.

3.  From the Campus page, select a campus.

    For example: Demo campus

4.  To create a CMN campus, navigate to **All** &gt; **CMN Location** and open the open the Location table \(cmn\_location\) and select **New**.

5.  On the Location form, fill in the form fields:

    -   Name: Name of the campus.
    -   Street: Street where the campus is located.
    -   City: Address of the campus.
    -   State/Province: Stat where the campus resides.
    -   Country: Country where the campus is located.
    -   Parent: Parent-child hierarchy. For example, Campus is the Parent and Buildings belonging to a Campus will be the child. For more information, see [Configure location migration hierarchy](../../workplace-service-delivery/task/add-location-migration-hierarchy.md).
    -   Latitude: Latitude coordinates of a campus location.
    -   Longitude: Longitude coordinates of a campus location.
6.  Select **Submit**.

7.  Select and open the **Demo Campus** that you created in step 3.

8.  Select **Synchronize with CMN Locations**.

    ![Campus showing the Synchronize with CMN location button.](../images/wsd-synchronize-with-CMN-Locations-tab.png)

9.  On the synchronization record form, search and select the CMN campus that you created in step 5.

    ![Search and select a CMN campus on the Synchronization record form.](../images/wsd-sync-campus-2.png)

10. Select **Update** to map the Indoor Mapping campus with the CMN campus.

    The location record is updated in the CMN Locations table.

11. Navigate to **All** &gt; **Tables** and search for the synchronization record.

    Make sure that the Indoor Mapping campus name matches with the CMN Location Campus.

12. Navigate to **Indoor Mapping** &gt; **Campuses**.

13. Select the Indoor Mapping campus that you want to synchronize.

14. Select Indoor Map / CMN Location Synchronization to run the sync script.

15. The synchronization record form synchronizes the campus and moves to synchronize the buildings in a campus and shows the following prefilled data.

    | | |
    |---|---|
    |Indoor Map Campus|Name of the Indoor Mapping campus is selected by default.|
    |CMN Location Campus|Name of the CMN Location campus is selected by default.|
    |State|Building|
    |Domain|Global|

16. From the Building related list, select an operation from the Operation column and right-click to change the suggested operation.

    ![Building synchronization page showing the proposed Create operation.](../images/wsd-ind-mapping-cmn-sync-form.png)

    Following options are available:

    -   **Create**: Indicates that a corresponding CMN building doesn’t exist in Indoor Mapping, and a new record should be created. The location name used in CMN location should match with the the location name in Indoor Mapping.
    -   **Link**: Indicates that a matching record from CMN location is found in Indoor Mapping. Select this option to link the CMN building with Indoor Mapping.
    -   **Ignore**: Indicates that the CMN location can be ignored and won't be available in Indoor Mapping.
    -   **Keep**: Indicates that the CMN location is already linked to a corresponding record in Indoor Mapping. This record can’t be changed in the synchronization process.
17. Select **Apply &amp; Next**.

18. If you selected **Create** operation in Step 16, a building is created in the CMN location and the status is shown as **Queued**.

    The synchronization is executed according to the selection operation \(Create, Link, Keep, or Ignore\).

    **Note:** The synchronization process is executed and the operation is Queued till it completes. A synchronization operation must complete before starting a new one. Don't select **Update** as synchronization of location records at this stage is incomplete. Wait for the operation to complete or till the page is refreshed with status **Complete**.

    ![Synchronization script synchronizes the Indoor Mapping buildings with CMN buildings.](../images/wsd-cmn-sync-create-building.png)

19. Select **Refresh** to refresh the page and see if synchronization is complete for a building.

20. Synchronization state moves to Floors.

    | | |
    |---|---|
    |Indoor Map Campus|Name of the Indoor Mapping campus is selected by default.|
    |CMN Location Campus|Name of the CMN Location campus is selected by default.|
    |State|Floor|
    |Domain|Global|

    ![Sync Script synchronizes the Indoor Maps Floors with CMN Location Floors records.](../images/wsd-sync-ind-map-with-cmn-floors.png)

21. Select the Floors that you want to synchronize.

    Select the required operation from the proposed operation \(Create, Link, Keep, Ignore\) from the Related list.

22. Select **Apply &amp; Next**.

    **Note:** The synchronization process is executed as per the proposed operation \(Create, Link, Keep, or Ignore\). Wait till the operation completes and is queued. A synchronization operation must be complete before starting a new one. Don' select **Update** as synchronization at this stage is incomplete.

23. Synchronization state moves to **Type** synchronize Indoor Mapping Place types with CMN Location Place types.

    | | |
    |---|---|
    |Indoor Map Campus|Name of the Indoor Mapping campus is selected by default.|
    |CMN Location Campus|Name of the CMN Location campus is selected by default.|
    |State|Type|
    |Domain|Global|

    ![Synchronization of CMN places with Indoor Mapping Place types.](../images/wsd-cmn-sync-place-types.png)

    Select the required operation from the proposed operation \(Create, Link, Keep, Ignore\) from the Related list.

    If the CMN Location Place Type column is empty, create a CMN Location Place Type to map it to corresponding Indoor Mapping Place Types. For more information, see [Add CMN locations and map it to Indoor Mapping Place types](enable-cmn-location-types.md).

    ![Create CMN Location Place Type if they are missing while running the sync script.](../images/wsd-cmn-sync-place-types-desks.png)

24. Select **Apply &amp; Next**.

    **Note:** The synchronization process is executed as per the proposed operation. A synchronization operation must be complete before starting a new one. Don' select **Update** as synchronization at this stage is incomplete. Wait for the operation to complete.

25. The Synchronization state moves to **Places**.

    | | |
    |---|---|
    |Indoor Map Campus|Name of the Indoor Mapping campus is selected by default.|
    |CMN Location Campus|Name of the CMN Location campus is selected by default.|
    |State|Places|
    |Domain|Global|

    Select the required operation from the proposed operation \(Create, Link, Keep, Ignore\) from the Related list.

    **Note:** The synchronization process is executed as per the proposed operation. Wait till the operation completes. **Remaining Operations** shows the progress of the synchronization process. A synchronization operation must be complete before starting a new one. Don' select **Update** as synchronization at this stage is incomplete. Wait for the operation to complete.

26. Synchronization moves to **Complete** when all location records are synchronized.

27. After synchronization is complete, verify that the CMN location Campus, buildings, Floors and Places are synchronized.

    1.  To verify that the Place Types are linked, navigate to the Indoor Mapping Campus that you created in step 1 \(**Demo campus**\) and open the campus form.

    2.  Notice that the **Location** field is having the Campus name **Demo Campus**.

        This is a reference to the Campus in CMN location and shows that the Indoor Mapping campus is linked to the CMN location.

    3.  The **Unlink Campus** tab is available after the synchronization is complete and the Indoor Mapping map object is linked to the CMN location indicating that the linking is complete.

        Unlinking a campus unlinks all the buildings associated with a campus. Unlinking a building unlinks all the floors and spaces associated with a building. Unlinking a floor unlinks the spaces associated with a floor.

28. When the records are fully synchronized, the CMN Locations table shows the Location source column as Indoor Mapping.

    ![Locations table.](../images/wsd-synchronized-cmn-location-source.png)

29. To make a synchronization record as favorite, complete the steps.

    1.  Select the List controls icon \(![List controls icon.](../images/wsd-additional_icon.png)\) and select **Create favorite** to easily locate your sync record.

    2.  Select a color, if required.

    3.  Select **Ok**.

    For more information about synchronizing Indoor Mapping locations with Workplace Indoor Mapping, see [Synchronize Indoor Mapping with Workplace Service Delivery](synchronize-ind-mapping-wsd.md).

30. To add a place or location to an Indoor Mapping building, navigate to **All** &gt; **Indoor Mapping** &gt; **Map Studio**.

    1.  Select the building to add a place or location.

    2.  Select Manage places.

    3.  Select the floor to be displayed on a map.

    4.  Click **New point** or **New polygon** to start creating places and new points of interest.

    For more information, see [Manage places](manage-buildings.md).

31. After adding the places or locations in Indoor Mapping Map Studio, synchronize the places with CMN locations for a building or campus.


**Parent Topic:**[Synchronize Indoor Mapping with CMN Locations](../concept/sync-cmn-location.md)

**Previous topic:**[Add CMN locations and map it to Indoor Mapping Place types](enable-cmn-location-types.md)

**Next topic:**[Using enhanced synchronization](../concept/using-enhanced-sync.md)

