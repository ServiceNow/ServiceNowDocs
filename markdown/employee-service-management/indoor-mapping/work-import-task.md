---
title: Work on an import task
description: Select a source and resolve issues to complete the import task for a floor plan.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/indoor-mapping/work-import-task.html
release: zurich
product: Indoor Mapping
classification: indoor-mapping
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Bulk update floor plans, Manage CAD source files, Indoor Mapping, Workplace Service Delivery, Employee Service Management]
---

# Work on an import task

Select a source and resolve issues to complete the import task for a floor plan.

## Before you begin

Role required: sn\_map\_core.map\_admin, sn\_map\_core.map\_editor

## About this task

Import tasks are automated processes, but sometimes require your inputs. If an import task can’t proceed without your input, the **State** field is set to `Waiting user input`.

The required input is based on the **Step** field and more information is added to the work notes of the record.

-   Source retrieval: This step is required to link the CAD file to its source in the Workplace Service Delivery application.
-   Georeference: This step is required to position and scale your source floor plan on the map.
-   Configuration: This step is required to select the layers and place types for the floor plan.

## Procedure

1.  Navigate to **All** &gt; **Indoor Mapping** &gt; **Bulk imports** &gt; **Pending tasks**.

2.  From the Floor plan import tasks list, select the task that you want to work on.

    You can also select an import task from the import group. For more information about import groups, see [Create an Import Group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/indoor-mapping/create-import-group.md).

3.  If the import task is at the `Source retrieval` step, select a source for the import task.

    If the file name is the same as the source, the system automatically selects the source and moves to the next step. Otherwise, the Automate map updates agentic workflow is triggered to retrieve the source. The Map Admin Agent autonomously retrieves sources for the uploaded CAD file. If the correct source is found, the agent sets the source and resumes the task. If the source isn't found, the agent moves the task to the `Waiting user input` state.

    For more information about the Automate map updates AI agentic workflow, see [Automate map updates agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/now-assist-for-wsd/automate-map-updates-agent-ai.md).

    **Note:** If **Supervised AI execution** was selected while creating the import group, you must select **Trigger AI Agent** to trigger the Automate map updates agentic workflow.

    1.  In the source field, select the source that is related to the attached source file.

        For example, if the source file `A-Floor3.dwg` is for the third floor of Building A, select `Building A- Floor 3` as the source.

    2.  Select **Continue**.

4.  If the import task is at the `GeoReference` step, configure the GeoReference of the floor plan.

    If the GeoReference of the floor plan is already configured, the system automatically moves to the next step.

    1.  Open the floor map by selecting **Open in Map Studio**.

    2.  Set the GeoReference of the floor plan.

        For more information about setting the GeoReference, see [Georeference your floor plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/indoor-mapping/georeference-floor-plan.md).

    3.  Select **Continue**.

5.  If the import task is at the `Configuration` step, configure the layers and places on the floor plan.

    If the layers and places are already configured, the system automatically moves to the next step.

    1.  Open the floor map by selecting **Open in Map Studio**.

    2.  Configure the layers and places on the floor plan.

        For more information about configuring layers and places, see the following topics:

        -   [Configure layers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/indoor-mapping/wsd-edit-layers.md)
        -   [Configure places](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/indoor-mapping/edit-places.md)
    3.  Select **Continue**.


**Parent Topic:**[Bulk update floor plans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/indoor-mapping/bulk-import-cad-files.md)

**Previous topic:**[Create an Import Group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/indoor-mapping/create-import-group.md)

**Next topic:**[Compute CAD file properties to extract space or room surface area](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/indoor-mapping/compute-cad-properties.md)

