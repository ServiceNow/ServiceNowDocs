---
title: Providing your workplace data
description: In the Workplace Core application, provide data related to your workplace locations so you can efficiently assign shifts to employees and designate workspaces for these shifts.
locale: en-US
release: xanadu
product: Workplace Core
classification: workplace-core
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure Workplace Core, Workplace Core, Workplace Service Delivery, Employee Service Management]
---

# Providing your workplace data

In the Workplace Core application, provide data related to your workplace locations so you can efficiently assign shifts to employees and designate workspaces for these shifts.

## Workspace Record

The information available for each workspace record is:

-   Region
-   Site
-   Campus
-   Building
-   Floor
-   Area
-   Space

Each designation should use a unique identifier. For example, if you are indicating the fourth floor in building 7, you would name the floor "7-4" rather than just "4".

## Entering data for several work sites

If you have a large organization, you might want to consider using a spreadsheet to contain the more global record information such as regions, buildings, and sites so you can avoid having to manually input repeated information for each workspace record. You can either export the information you've already entered into the application into a spreadsheet or use that information in an existing workspace spreadsheet. You would then import the spreadsheet that contains the full workspace data into the application in bulk form.

-   If you have an existing spreadsheet, you would first manually convert the column headers and data of the global information to match the ServiceNow record names and identifier numbers. You would then do a bulk import of that data into the Workplace Core application so you can assign workspaces.

    For example, say your organization's spreadsheet uses the name "Location" for Sites or "Bldg 1" for every building 1 on every site. You would have to change the spreadsheet column header "Location" to "Sites" and change each "Bldg 1" to the unique identifier from the Workplace Core application records.

-   If you don't have an existing spreadsheet, you would enter the repeated global information that you don't want to have to input manually for each space. The data for each field should have a unique identifier. You would then export the information from the application into a spreadsheet where you would have to input only the space information manually.


## Floor plans

The ServiceNow AI Platform supports Drawing eXchange Format \(.dxf\) files for floor plans. You can select the layers you need for end-user floorplans and configure the attributes \(tags\) you want assigned to fields. For information about how to export an AutoCAD .dwg file to a Drawing eXchange Format \(.dxf\) file, see the documentation for your version of AutoCAD.

Prior to uploading a .dxf file, work with your AutoCAD designers to ensure the following:

-   The file uses block references and not single-line or multi-line text for space labels.
-   The blocks attributes have human-understandable tags.
-   The block references have attribute values appropriately set.

    **Note:** Using blocks is highly recommended. Do not use text objects.


Uploading a floor plan creates a floor record. All the workspaces of the floor are automatically added to the Spaces related list of the floor record.

-   **[Create records for your workplace data](../task/create-records-of-workplace-data-wsd.md)**  
Create individual records of your workspaces, floors, office buildings, and workplace locations within the Workplace Core application. Either insert new data or add records to the existing workplace data.
-   **[Upload a workplace floor plan](../task/upload-workplace-floor-map-wsd.md)**  
Upload Drawing eXchange Format \(.dxf\) files of floor plans that you can configure and use to reserve space for your employees.
-   **[Update a workplace floor plan](../task/edit-workplace-floor-map-wsd.md)**  
Update a workplace floor plan by uploading a new plan.

**Parent Topic:**[Configure Workplace Core](configure-wsd.md)

**Related topics**  


[Install Workplace Core](../task/install-workplace-service-delivery.md)

[Configuring spreadsheets to import workplace data](importing-workspace-data-wsd.md#)

[Activate Virtual Agent for Workplace Service Delivery](../task/actuvate-va-for-wsd.md)

