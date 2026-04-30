---
title: Synchronize Indoor Mapping with Workplace Service Delivery
description: Synchronize Indoor Mapping locations and map data objects with Workplace Service Delivery campus, buildings, floors, and spaces.
locale: en-US
release: xanadu
product: Indoor Mapping
classification: indoor-mapping
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 11
breadcrumb: [Manage map objects and data, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Synchronize Indoor Mapping with Workplace Service Delivery

Synchronize Indoor Mapping locations and map data objects with Workplace Service Delivery campus, buildings, floors, and spaces.

## Before you begin

The changes that you make to Workplace Service Delivery building, floor, and space records are not updated automatically with the Indoor Mapping map data and objects. To update the changes, synchronize Indoor Mapping campus, buildings, floors, and place types with Workplace Service Delivery \(WSD\) location records.

**Note:** After installing the Indoor Mapping application and updating locations on your map, run the synchronization utility to synchronize Indoor Mapping location records with Workplace Service Delivery locations. Run the synchronization utility when you add, update, or remove locations from Workplace Service Delivery or update locations or map objects in Indoor Mapping Map Studio.

The synchronization process is a five-step process. Take appropriate actions as required during the synchronization process:

-   Cleaning: The Cleaning step in the synchronization utility isn’t available initially when you run the synchronization wizard for the first time. It is available only for spaces that are deleted while making updates to the Indoor Mapping Map studio.

    **Note:** A **Cleaning** step can also appear as your first step in the synchronization utility if a location record is changed or updated in the Indoor Mapping Map studio. This step is shown for location records that are synchronized but are updated or modified later on after the synchronization process.

-   Building Sync: Option to synchronize a building in a campus in Indoor Mapping and Workplace Service Delivery.
-   Floors Sync: Option to synchronize the floors in a building in Indoor Mapping and Workplace Service Delivery floor record.
-   Types Sync: Option to link and map Indoor Mapping place types to corresponding spaces in Workplace Service Delivery.This option shows the Indoor Mapping place types that are not linked to a Workplace Service Delivery spaces. You can select the **Link** operation in the synchronization utility to link the location records.
-   Spaces Sync: Option to synchronize the spaces available on a floor.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Space Mapping** &gt; **Indoor Mapping Administration** &gt; **Indoor Map / WSD Synchronizations**.

    The Indoor Map / WSD Synchronizations page displays existing synchronization records for Indoor Mapping and Workplace Service Delivery.

2.  Select **New**.

    **Note:** You must create or have an existing Campus, Region, and Site in Workplace Service Delivery \(WSD\).

    On the form, fill in the fields.

<table id="table_o2l_p42_hwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

WSD Campus

</td><td>

Option to select a Workplace Service Delivery campus.

 Select the lookup list icon \(![Lookup list icon.](../../workplace-case-mgmt/image/search-icon.png)\) to search and select a Workplace Service Delivery campus.

 Make sure that the time zone of the campus matches with the Region of your Indoor Mapping campus.

</td></tr></tbody>
</table>3.  Select **Submit**.

    A new synchronization record is created.

4.  From the synchronization record page, select the Indoor Mapping Campus that you want to synchronize with the Workplace Service Delivery Campus, if they aren’t already synchronized.

    The new synchronize script record opens \(for Example: IMWS0005278\).

    On the form, fill in the form fields.

    |Field|Description|
    |-----|-----------|
    |WSD Campus|Campus created in Step 3.|
    |Indoor Map Campus|Indoor Map campus. Search using the lookup list icon \(![Lookup list icon](../../workplace-case-mgmt/image/search-icon.png)\) to select the Indoor Mapping campus information or search for an Indoor Map campus.|

    The campuses are synchronized.

5.  The synchronization utility proceeds to synchronize a building in a campus.

    This is the first step in the synchronization process if you are running the synchronization utility for the first time.

    ![Synchronization utility showing proposed operation to synchronize a building.](../images/wsd-building-synchronization.png)

    | | |
    |---|---|
    |WSD Campus|Name of the Workplace Service Delivery campus.|
    |Indoor Map Campus|Name of the Indoor Mapping campus.|
    |State|Building|

    **Note:** A **Cleaning** step can also appear as your first step in the synchronization utility if changes or additions are made to Indoor Mapping locations records or map objects after they are synchronized.

    You can change the proposed operation in the synchronization utility. Select an operation from the Operation column and right-click to change it.

    -   If a new building is detected, **Create** operation is proposed in the Building related list Operation column. Indicates that a corresponding Indoor Mapping map record doesn’t exist in Workplace Service Delivery, and a new record should be created. The location name used in Workplace Service Delivery should be similar to the location name in Indoor Mapping
    -   **Link**: Indicates that a matching record from Indoor Mapping is found in Workplace Service Delivery based on the location name. The Indoor Mapping record is linked to an existing object in Workplace Service Delivery \(WSD\). After linking, the Workplace Service Delivery location name is shown in Indoor Mapping.
    -   **Ignore**: Indicates that the Indoor Mapping record is ignored and won’t be available in Workplace Service Delivery.
    -   **Keep**: Indicates that the Indoor Mapping record is already linked to a Workplace Service Delivery record. This record can’t be changed in the synchronization process. If you want to unlink a record, select a location record in Workplace Core and select **Unlink**. After unlinking, the location record doesn't show the **Keep** operation.
    -   **Cleaning**: Two synchronization operations are available when performing the cleaning activity on a location record:
        -   **Retire**: Option to set the status of Workplace Service Delivery location to **Retire**.

            **Note:** This action removes all references to Indoor Mapping and is deactivated in the Workplace Core location table. The object is not available for subsequent synchronizations.

        -   **Unlink**: Option to unlink or remove references to Indoor Mapping. The location remains active in Workplace Core and can be reused in subsequent synchronizations.
6.  Select **Apply &amp; Next**.

    The synchronization process shows anomalies if a record is invalid. Go to the instance log page to verify the reason for anomaly.

    The building records are synchronized and the status is shown as **Queued**.

    **Note:** The synchronization utility takes sometime to synchronize a location record. Wait till the operation completes and the page is refreshed with updated status. Don't select **Update** as synchronization at this stage is incomplete.

7.  After building records are synchronized, the synchronization utility **State** moves to **Floor**.

    | | |
    |---|---|
    |WSD Campus|Name of the Workplace Service Delivery campus.|
    |Indoor Map Campus|Name of the Indoor Mapping campus is selected by default.|
    |State|Building|

    The floor records are ready to be synchronized and the status is shown as **Queued**.

    **Note:** The synchronization utility takes sometime to synchronize a location record. Please wait till a synchronization operation completes before you proceed to the next step in the synchronization utility. Don't select **Update** as synchronization at this stage is incomplete. The synchronization process shows anomalies if a record is invalid in the Anomaly column of the Related list.

8.  Select **Apply &amp; Next**.

    **Note:** The synchronization process is executed as per the proposed operation. Wait till a synchronization operation completes before you proceed to the next step in the synchronization utility. Don't select **Update** as synchronization at this stage is incomplete. A synchronization operation must be complete before starting a new one.

9.  Proceed with **Type** synchronization.

    Indoor Mapping places that aren’t linked to Workplace Service Delivery spaces are ignored from the synchronization process. This step ensures that all Indoor Mapping place types are linked to appropriate Workplace Service Delivery spaces.

    -   By default, new location **Types** are linked to **Miscellaneous**.
    -   In the Related List, select the Operation column, and make inline edits.
    -   Right-click and selecting **Link**, **Ignore**, or **Keep** to change the proposed operation.
10. Select **Apply &amp; Next**.

    **Note:** The synchronization process is executed as per the proposed operation. Wait till a synchronization operation completes before you proceed to the next step in the synchronization utility. Don't select **Update** as synchronization at this stage is incomplete. A synchronization operation must be complete before starting a new one.

11. The synchronization utility shows the **Updated Space Type on Link or Keep?** option.

    This option prevents overwriting location records that are already synchronized.

    For example, a place type \(Auditorium\) in Indoor Mapping is linked to a **Miscellaneous** Workplace Service Delivery Space Type. If this space type is later changed to a Meeting room in Workplace Service Delivery, update this location record by selecting **Updated Space Type on Link or Keep?**. This prevents overwriting the location records later on in the synchronization process when **Link** and **Keep** operations are selected. A corresponding Workplace Service Delivery location is only added in Indoor Mapping when **Create** option is selected.

12. The synchronization utility state moves to **Space** synchronization.

    | | |
    |---|---|
    |WSD Campus|Name of the Workplace Service Delivery campus.|
    |Indoor Map Campus|Name of the Indoor Mapping campus is selected by default.|
    |State|Spaces|

13. Proceed with the suggested operations **Link**, **Create**, **Ignore**, or **Keep**.

14. Select **Apply &amp; Next**.

    **Note:** The synchronization process is executed as per the proposed operation. The **Remaining operations** field shows the progress of synchronization. Wait till an operation completes. Select **Refresh** on the Related lists to get the synchronized status of a record.

    A synchronization operation must be complete before starting a new one. Don't select **Update** as synchronization at this stage is incomplete.

15. If any updates or changes are made to Indoor Mapping location or map data objects in the Map studio after a location record is already synchronized, a **Cleaning** step appears in the Synchronization utility wizard as your first step.

    Location record that is deleted or updated in Indoor Mapping Map studio after a locations is synchronized are shown for you to take appropriate action. By default, the **Retire** operation is proposed. It can be changed an **Unlink** operation.

    ![Synchronization utility showing the Cleaning step and the proposed operation to Retire and Unlink.](../images/wsd-sync-retire-places.png)

16. When all location records are synchronized in a campus, the synchronization **State** moves to **Complete**.

17. Enable the Default view in the Indoor Mapping Map studio.

    **Note:** Enabling the default view in Indoor Mapping is a mandatory step. The Default view is required to render the map in Workplace Service Delivery. For more information about Default view, see [Edit with view editor](edit-with-view-editor.md).

18. Configure notifications to be sent to workplace users every time a change or update is made to synchronized location records.

    ![Campus form showing Send syn script notification.](../images/wsd-send-sync-script-option.png)

    1.  Enable notifications on the Workplace Core Campus Table.

    2.  Navigate to **All** &gt; **Workplace Core** &gt; **Administration** &gt; **Campuses**.

    3.  On the campus page, select the gear settings icon \(![Gear settings icon to change the settings for a campus.](../../workplace-safety-mgmt/images/wsd-gear-settings-icon.png)\).

    4.  In the Personalized list columns, select **Send Sync Script Notification** and add it to the Selected column.

    5.  Select **Ok**.

    6.  On the campus page, from the list of campuses, select a campus.

    7.  In the **Managed by group** field, select the lookup list icon \( ![Look up list icon to search for a workplace group.](../../workplace-connectors/images/wsd-lookup-list-icon.png)\) to search for a workplace group and add the group.

    8.  In **Managed by** field, select the lookup list icon \(![Look up list icon to search for a workplace user.](../../workplace-connectors/images/wsd-lookup-list-icon.png)\) to search for a workplace user and add the workplace user.

    9.  Select the **Send sync script notification** checkbox.

        Workplace users are notified daily whenever a location record is updated and when unsynchronized data is detected.

19. Launch the synchronize utility to update location records with the latest changes.

    When changes are done in Indoor Mapping Map Studio, updated locations and map objects are not automatically synchronized with Workplace Service Delivery Spaces. It is necessary to manually run the Synchronization utility.

    Enable the **Synchronize** and **Unlink campus** on a Workplace Service Delivery campus.

    1.  Navigate to **All** &gt; **Workplace Core** &gt; **Space Administration** &gt; **Campuses**.

    2.  Select a campus from the list of campuses.

        For example, campus 501.

    3.  On the Campus form details page, select the additional actions menu icon \(![Additional list.](../../human-resources/image/additional-actions-icon.png)\).

    4.  Select **View** &gt; **Workplace Indoor Mapping** campus.

    5.  Select the time zone of your campus.

    6.  Add the Indoor Mapping campus name to the Indoor Mapping campus field.

    7.  Select **Save** to link the WSD Campus and Indoor Mapping Campus.

    8.  After saving, the following buttons are available:

        -   **Synchronize**: Option to navigate to the Indoor Map/WSD synchronizations page.
        -   **Unlink Campus**: Option to remove the link or mapping between Workplace Service Delivery campus and Indoor Mapping campus. The location remains active in Workplace Core and can be reused in subsequent synchronizations.

            The **Unlink Campus** tab is available after the synchronization is complete and the Indoor Mapping map object is linked to WSD locations indicating that the linking is complete. Unlinking a campus unlinks all the buildings associated with a campus. Unlinking a building unlinks all the floors and spaces associated with a building. Unlinking a floor unlinks the spaces associated with a floor.


**Parent Topic:**[Manage map objects and data](../concept/using-indoor-mapping.md)

**Previous topic:**[Keyboard shortcuts](keyboard-shortcuts.md)

**Next topic:**[Synchronize Indoor Mapping with CMN Locations](../concept/sync-cmn-location.md)

