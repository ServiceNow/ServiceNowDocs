---
title: Create a campus with buildings and floors
description: Create your first Indoor Mapping campus and add a few buildings and floors to it using the Indoor Mapping Map Studio. Import your CAD and raster image source files to complete your campus configuration.
locale: en-US
release: zurich
product: Indoor Mapping
classification: indoor-mapping
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Manage map objects and data, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Create a campus with buildings and floors

Create your first Indoor Mapping campus and add a few buildings and floors to it using the Indoor Mapping Map Studio. Import your CAD and raster image source files to complete your campus configuration.

## Before you begin

Install Indoor Mapping and configure basic information about your campus, building, or floors in the Map Studio by importing the floor plan sources.

**Note:** Upload and Import AutoCAD \(DWF or DXF\) or raster image \(PNG\) source files in the Map Studio.

Before you begin to use the Map Studio, ensure that your floor plans meet the following guidelines:

-   [AutoCAD requirements](https://www.servicenow.com/community/presession?client_id=0oawkyhdomINvSrdm0x7&redirect_uri=https%3A%2F%2Fwww.servicenow.com%2Fcommunity%2Fs%2Fauth%2Foauth2callback%2Fproviderid%2Fbounce&response_type=code&state=GjqF2-Ia5kXMgeZuqaG81-G_ohfcv2IUbX-wmyEvMbJaItnYyRu7Gh6ztaL5osYy7JCk1YFzi-pffQNbtsby63KdGOMPq-RCKCzc6h9u_b_gQMO0q_5vK2WzDj-N3kUVpFIG_GOD2GvqHSPIzW74Eq-QPYJyjyJYr0tf8ug8CU-kX7P-zxI5lh9SltHEBxe6r5SCm5peKWsuZRbAucPs3DNVFaCEAoVfdV6mYZbW9n6aUrvv9zpQb9zf2o-udHxm&scope=openid&referer=https%3A%2F%2Fwww.servicenow.com%2Fcommunity%2Fwsd-blog%2Fcad-file-guidelines-for-indoor-mapping%2Fba-p%2F2266775)
-   [Raster requirements](https://www.servicenow.com/community/wsd-blog/png-guidelines-for-indoor-mapping/ba-p/2266959)

Role required: map admin, map editor, map editor limited

## Procedure

1.  Navigate to **All** &gt; **Indoor Mapping** &gt; **Map Studio**.

2.  Additionally, if you have existing campuses, you can search for a campus on the Map Studio home page.

    1.  Select the **Search** icon \(![search icon](../../workplace-case-mgmt/image/search-icon.png)\) to search for a campus that you want to update or switch to.

3.  To create a campus, select the **Get Started** tab.

    On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Country|Country or region where the campus is located.|
    |Campus Name|Name of the campus.|
    |Address|Precise campus location address as it appears on the map.|

4.  Select **Edit** to edit the campus name and address.

5.  Select **Continue** to add your first building.

6.  Provide the building name.

    Building address is pr-efilled.

7.  Click **Continue**.

8.  Enter the name of the building and address.

9.  Click **Save**.

    Building boundaries are computed automatically.

10. In case, if you cannot find your newly created building on the map, you will see the following screen:

    ![Building location shown on the map](../images/campus-creation1.png)

11. Select **Continue**.

    **Note:** Your polygon must be at least around the building. It doesn't need to match the exact shape of the building.

12. At this stage, you can add additional buildings or edit the existing building details.

13. Select **+Add a building** to create additional buildings in your campus.

14. Navigate to **Manage Workplace** &gt; **Floor &amp; Floorplans** to add a floor or floors to your building.

15. Select your building.

    **Note:** Ensure to select a building as you can upload files at the Campus level. If you select a building, it will be visible at every levels as you can only import your files at the Outdoor level.

16. Select **Add a floor**.

    On the form, fill in the fields

    |Field|Description|
    |-----|-----------|
    |Building|Building name or number where the floor is located.|
    |Number|Floor level. Takes an integer or a numerical value.|
    |Name|Floor name or title|
    |Title|Title displayed on the floor controller.|

17. Click **Create**.

18. Repeat Steps 16-18 for each floor of your building.

19. Navigate to '**Manage Workplace** &gt; **Campus and buildings**.

    It is important that your campus encompasses or its boundaries are well adjusted for all buildings. The boundaries are automatically adjusted. For more information, see [Working with boundary editor](working-with-boundary-editor.md).

    Your campus is configured.

20. After your campus and buildings are created, you can start importing your CAD files or raster image floor plan source files.

21. In the Map Studio, navigate to **Manage workplace** &gt; **Floors and Floor plans**.

22. Locate your floor where you want to upload your CAD or raster file.

    \(Optional\) At this stage, floor plans can be uploaded and imported as AutoCAD \(DXF/DWG\) or raster image file \(PNG\) sources or you can import the files after creating a campus. Ensure that you've reviewed the design guidelines before importing the sources to the Map Studio. For more information about how to import, see [Import CAD files to Map Studio](CAD-file-import.md) and [Import Raster files](import-raster-files.md).

23. After importing a CAD or raster file, select **Manage Workplace** and select **Overview**.

24. Select the building that you created.

    Your map is configured and available on the Map Studio.


**Parent Topic:**[Manage map objects and data](../concept/using-indoor-mapping.md)

**Previous topic:**[Manage map objects and data](../concept/using-indoor-mapping.md)

**Next topic:**[Working with boundary editor](working-with-boundary-editor.md)

