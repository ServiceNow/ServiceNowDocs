---
title: Map multiple application services suggested by classic Service Mapping
description: You can map multiple application services identified and suggested by Service Mapping in a single operation. This method suits your organization if you do not have much information about application services.
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 9
breadcrumb: [Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Map multiple application services suggested by classic Service Mapping

You can map multiple application services identified and suggested by Service Mapping in a single operation. This method suits your organization if you do not have much information about application services.

## Before you begin

Role required: service\_mapping\_admin

## About this task

You must have Service Mapping enabled to map or review service instances.

Immediately after you complete the Service Mapping setup, Service Mapping automatically creates potential application services referred to as candidates:

1.  Service Mapping extracts entries directly from load balancers on your network.

2.  Service Mapping converts load balancer entries into potential entry points and stores them in the Candidate Entry Points \[sa\_cand\_entry\_point\] table.

    Service Mapping also creates candidate entry points based on Netflow and TCP and stores them in the same table.

    An entry point is a point where clients access a service instance. Service Mapping starts the mapping process from this point. For example, to map your electronic mailing service instance, define an IP address or host name of the email server as an entry point.

3.  Service Mapping checks that potential entry points created from Netflow and VPC logs are unique and not in use by any existing application services to avoid duplication.
4.  Service Mapping creates a service instance candidate for each entry point.

    Not all candidate service instances correlate to actual service instances. Service Mapping filters out unlikely candidates by applying an algorithm that takes into account such parameters as empty IP addresses, port numbers, and the load balancer VIP hit counts less than 1000. Service Mapping stores candidates in the Candidate Entry Point \[sa\_cand\_entry\_point\] table in the CMDB.


During the discovery and mapping process, Service Mapping creates a service instance from each candidate and assigns it the entry point retrieved from the candidate. While mapping in bulk is an effective and fast way to create numerous service instances, the result of the bulk mapping is not precise. There may be some false or duplicate service instances created by mistake because the data from the load balancer is raw. During the review and approval process, you review all mapped service instances and get rid of the ones that were erroneously created.

You can further filter the list of candidates by selecting specific ones to include in or exclude from discovery. Mapping only selected candidates provides the following advantages:

-   Reduces the discovery time
-   Minimizes the number of potential irrelevant application services

You can remove the unwanted candidates from the list using these methods either by filtering them out or deleting them from the Candidate Entry Point \[sa\_cand\_entry\_point\] table. In both cases, you can bring hidden or deleted candidates back to the list.

## Procedure

1.  Navigate to **All** &gt; **Service Mapping** &gt; **Home**.

    The Home page displays only information on service instances that Service Mapping can discover or already discovered. The Home page does not display information on service instances that are created manually or using the API.

2.  Verify that Service Mapping is set up and ready for discovery.

    If some obligatory configurations are missing, the error displays at the top of the window.

    1.  Click the link in the error or click the **Readiness Checklist** icon \(![Readiness Checklist icon](../image/ReadinessChecklistErrorIcon.png)\).

    2.  In the Service Mapping Readiness Checklist window, click the link next to the setup category with the error icon \(![Error icon](../image/BulkMappingSetupErrorIcon.png)\).

        You cannot perform discovery and mapping unless there are no errors in the Readiness Checklist window.

    3.  Perform the necessary action to complete the setup.

        For example, configure missing credentials.

3.  To map all application services suggested by Service Mapping, click **Discover All** or select them individually under the Action on selected rows button then click **Discover Selected**.

4.  To map selected application services suggested by Service Mapping:

    1.  Click **Additional options** under the **Map** tile.

    2.  Select **View Candidates List**.

    3.  Display candidates based on traffic-based connections, remove the condition that filters out candidates retrieved from load balancers or imported from a CSV file.

        ![Display service instance candidates based on traffic-based connections](../image/BSCandidatesDisplayNetstat.png)

        The candidate list shows candidates with the source attribute **netstat**.

    4.  Review the list of candidates to decide which ones you want to discover as application services.

    5.  Create application services from the relevant candidates:

<table id="table_sp1_1cn_j2b"><tbody><tr><td>

If you want to create application services from most of the candidates

</td><td>

1.  Filter out irrelevant candidates by selecting them and clicking **Actions on selected rows**, and then clicking **Ignore Selected**.

The irrelevant candidates are hidden from the list.

**Note:** To show candidates you previously filtered out, set the **Ignore** filtering condition to **true**.

2.  Alternatively, delete irrelevant candidates by selecting them and clicking **Actions on selected rows**, and then selecting **Delete**.

The irrelevant candidates are removed from the Candidate Entry Point \[sa\_cand\_entry\_point\] table containing candidates.

**Note:** Service Mapping recreates deleted candidates every time Discovery performs horizontal discovery of the same load balancers or you reimport candidates from the same CSV file.

3.  Click **Discover All**.


</td></tr><tr><td>

If you want to create application services only from several candidates

</td><td>

1.  Select the check boxes next to the relevant candidates.
2.  Click **Actions on selected rows** at the bottom of the screen.
3.  Click **Discover selected**.


</td></tr></tbody>
</table>    Service Mapping starts discovery of all candidates and creates application services from them. If you have many candidates, the discovery may take some time.

    After the discovery process finishes, application services, which Service Mapping discovered without errors and with at least one discovered CI, appear under the **Approve** tile. application services discovered with errors appear under the **Fix** tile.


## What to do next

-   If the connection suggestions feature is enabled, Service Mapping does not automatically add any traffic-based connections to application services, providing suggestions instead. [Add or remove CIs for multiple application services using connection suggestions](manipulate-connections-suggestions-in-bulk.md).
-   Fix application services discovered with errors. For more information, see [Fix application service errors in bulk](fix-bus-serv-errors-by-category.md).
-   Review the list of created application services. If Service Mapping did not create some application services during bulk mapping as you expected, create them manually as described in [Map a single application service using classic Service Mapping](t_DefineNewBusinessService.md).
-   Send application services discovered without errors to their respective owners for approval. For more information, see [Send application service maps for review](send-business-service-for-review.md).
-   Make sure that the service instances aren't too large:

    -   Service Mapping doesn't offer to view CI list instead of a map for a service instance.
    -   There is no discovery message indicating that the service instance is too large: **The map does not display the entire service, because it is too large. The number of CI connections exceeded the allowed maximum.**
    If some application services are too large, resolve the service size issue:

    -   If you use customized discovery patterns and mapping results in very large service instances, modify the patterns so that they don't map irrelevant CIs.
    -   [Split the service into smaller services](add-segment-to-business-service-map.md).

-   **[Add or remove CIs for multiple application services using connection suggestions](manipulate-connections-suggestions-in-bulk.md)**  
If the discovery based on Predictive Intelligence is enabled, the newly mapped application services include only CIs and CI connections added by discovery patterns. Use connection suggestions to decide which configuration items \(CIs\) to include or exclude globally. Service Mapping then updates all relevant discovered application services to reflect your decisions.
-   **[Add CIs to multiple application services using connection rules](add-cis-connection-rules-multiple.md)**  
Create rules for automatically adding traffic-based connections and the CIs they lead to in discovered service instances. Create rules that add CIs to multiple application services.

**Parent Topic:**[Application service mapping using classic Service Mapping](../concept/c_DefineMapBusinessServices.md)

**Related topics**  


[Map application services using tags with classic Service Mapping](map-service-tag.md)

[Map multiple application services from a CSV file using classic Service Mapping](import-business-services-csv.md)

[Map a single application service using classic Service Mapping](t_DefineNewBusinessService.md)

[Fix application service errors in bulk](fix-bus-serv-errors-by-category.md)

[Fix errors in individual application service maps](fix-or-ignore-errors-business-service-map.md)

[Review and approval of application service maps](business-service-approval.md)

[Fine-tune application services to implement owner requests](review-implement-business-service-maps.md)

[Application service completion](../concept/advanced-business-service-definitions.md)

[Application service analysis and maintenance using classic Service Mapping](../concept/c_SvcPlanningAndAnalysisUsingMaps.md)

