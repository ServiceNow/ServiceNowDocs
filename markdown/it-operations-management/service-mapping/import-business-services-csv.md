---
title: Map multiple application services from a CSV file using classic Service Mapping
description: This method suits you if your organization has performed cross-organization mapping and analysis and collected some information about planned service instances. If so, you can organize the collected information in a specific order and save it as a CSV file. Service Mapping extracts information from this file and creates potential service instances referred to as service candidates.
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Map multiple application services from a CSV file using classic Service Mapping

This method suits you if your organization has performed cross-organization mapping and analysis and collected some information about planned service instances. If so, you can organize the collected information in a specific order and save it as a CSV file. Service Mapping extracts information from this file and creates potential service instances referred to as service candidates.

## Before you begin

Perform the procedure described in [Prepare a CSV file for mapping your candidates](prepare-csv-file.md).

Role required: service\_mapping\_admin

## About this task

You must have Service Mapping enabled to map or review service instances.

If necessary, you can import service candidates from multiple CSV files.

When reimporting service instance candidates, Service Mapping does not import candidates you chose to ignore earlier.

After Service Mapping discovers configuration items \(CIs\) belonging to your service instance for the first time, it then rediscovers CIs to find changes and updates. Create or modify discovery schedules to control how often Service Mapping rediscovers services or CIs.

## Procedure

1.  Navigate to **All** &gt; **Service Mapping** &gt; **Home**.

    The Home page displays only information on service instances that Service Mapping can discover or already discovered. The Home page does not display information on service instances that are created manually or using the API.

2.  Under the **Map** tile, select **Additional Options**.

3.  Select **Import Service Map List**.

    ![Map tile Additional Options.](../image/map-application-services-csv.png "Map tile Additional Options")

4.  In the Import CSV file window, select **Choose file**.

5.  Navigate to the CSV file to use for the import and select **Open**.

6.  Select **Import**.

    The imported service instance candidates are added to the list of candidates.

7.  Check that the overall number of service candidates on the **Map** tile increased by the expected number.

8.  On the **Map** tile, select **Map Your Services** to create application services from the candidates you imported from the CSV file.


## What to do next

-   Review the list of created application services. If Service Mapping did not create some application services during bulk mapping as you expected, create them manually as described in [Map a single application service using classic Service Mapping](t_DefineNewBusinessService.md).
-   Fix application services discovered with errors. For more information, see [Fix application service errors in bulk](fix-bus-serv-errors-by-category.md).
-   Send application services discovered without errors to their respective owners for approval. For more information, see [Send application service maps for review](send-business-service-for-review.md).

-   **[Prepare a CSV file for mapping your candidates](prepare-csv-file.md)**  
Organize information about potential application services \(candidates\) in your organization and save it in a CSV file.

**Parent Topic:**[Application service mapping using classic Service Mapping](../concept/c_DefineMapBusinessServices.md)

**Related topics**  


[Map multiple application services suggested by classic Service Mapping](map-business-services-in-bulk.md)

[Map application services using tags with classic Service Mapping](map-service-tag.md)

[Map a single application service using classic Service Mapping](t_DefineNewBusinessService.md)

[Fix application service errors in bulk](fix-bus-serv-errors-by-category.md)

[Fix errors in individual application service maps](fix-or-ignore-errors-business-service-map.md)

[Review and approval of application service maps](business-service-approval.md)

[Fine-tune application services to implement owner requests](review-implement-business-service-maps.md)

[Application service completion](../concept/advanced-business-service-definitions.md)

[Application service analysis and maintenance using classic Service Mapping](../concept/c_SvcPlanningAndAnalysisUsingMaps.md)

