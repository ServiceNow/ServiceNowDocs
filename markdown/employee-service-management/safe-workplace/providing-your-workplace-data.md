---
title: Providing your workplace data
description: In the Workplace Core application, provide data related to your workplace locations so you can efficiently assign shifts to employees and designate workspaces for these shifts.
locale: en-US
release: australia
product: Safe Workplace
classification: safe-workplace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Workplace Core, Safe Workplace, Health and Safety, Employee Service Management]
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

Each designation should use a unique identifier.

## Entering data for several work sites

Large organizations can use spreadsheets to store shared location data such as regions, buildings, sites, eliminating manual re-entry for each workspace. You can either export the information you have already entered into the application into a spreadsheet or use that information in an existing workspace spreadsheet. You can then import the spreadsheet that contains the full workspace data into the application in bulk form.

-   If you have an existing spreadsheet, you can manually convert the column headers and data of the global information to match the ServiceNow record names and identifier numbers. You can then do a bulk import of that data into the Workplace Core application so you can assign workspaces.

    For example, say your organization's spreadsheet uses the name "Location" for Sites or "Bldg 1" for every building 1 on every site. You have to change the spreadsheet column header "Location" to "Sites" and change each "Bldg 1" to the unique identifier from the Workplace Core application records.

-   If you don't have an existing spreadsheet, you can enter the repeated global information that you don't want to have to input manually for each space. The data for each field should have a unique identifier. You can then export the information from the application into a spreadsheet where you have to input only the space information manually.


## Floor plans

The ServiceNow AI Platform supports Drawing eXchange Format \(.dxf\) files for floor plans. You can select the layers you need for end-user floorplans and configure the attributes \(tags\) you want assigned to fields. For information about how to export an AutoCAD .dwg file to a Drawing eXchange Format \(.dxf\) file, see the documentation for your version of AutoCAD.

Before uploading a .dxf file, work with your AutoCAD designers to verify the following:

-   The file uses block references and not single-line or multi-line text for space labels.
-   The blocks attributes have human-understandable tags.
-   The block references have attribute values appropriately set.

    **Note:** Using blocks is highly recommended. Don’t use text objects.


Uploading a floor plan creates a floor record. All the workspaces of the floor are automatically added to the Spaces related list of the floor record.

-   **[Create records for your workplace data](../task/create-records-of-workplace-data-hr.md)**  
Create individual records of your workspaces, floors, office buildings, and workplace locations within the Workplace Core application. Either insert new data or add records to the existing workplace data.
-   **[Upload a workplace floor plan](../task/upload-workplace-floor-map.md)**  
Upload Drawing eXchange Format \(.dxf\) files of floor plans that you can configure and use to reserve space for your employees.
-   **[Update a workplace floor plan](../task/edit-workplace-floor-map.md)**  
Update a workplace floor plan by uploading a new plan.
-   **[Configuring spreadsheets to import workplace data](importing-workspace-data.md#)**  
Doing a bulk import of the data of all your workspaces into the Workplace Core application through a spreadsheet enables you to avoid manually entering redundant data for each workspace, which saves time and effort.
-   **[Import your workspaces data from an Excel spreadsheet](../task/import-excel-spreadsheet-workspace-data-hr.md)**  
Import your workspaces data from an Excel spreadsheet into the Workplace Core application.
-   **[Add a space type configuration](../task/add-space-type-configurations-hr.md)**  
Configure the different types of workspaces available in a workplace. You can add spaces based on different space types \(Workspace/Desk\). Space type enables employee to identify the different types of workspace available on a floor

**Parent Topic:**[Workplace Core](workplace-safety-mgmt-hr.md)

