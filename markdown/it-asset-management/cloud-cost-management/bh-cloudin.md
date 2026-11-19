---
title: Business hours
description: A Business Hours job identifies cloud resources running outside the hours your business needs them, and powers them off on a schedule you define. It helps you save costs because you stop paying for idle compute overnight or during other low-use periods.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/cloud-cost-management/bh-cloudin.html
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Explore, Cloud Cost Management, IT Asset Management, Asset Management]
---

# Business hours

A Business Hours job identifies cloud resources running outside the hours your business needs them, and powers them off on a schedule you define. It helps you save costs because you stop paying for idle compute overnight or during other low-use periods.

## Business hours policy workflow

Each successful Billing Download job triggers Business hours, along with the Budget forecast, Commitments, Rightsizing, and Unused resources, to analyze the spend and usage data. It also updates the actionable recommendations in the reports. The following infographic shows an example workflow of finance department business hours policy.

\[Omitted image "bh-policy-flow-diagram.png"\] Alt text: An example process flow for Business hours for the finance department

The Business hours process runs as follows:

1.  For each Business hours policy, the system queries the CMDB to identify resources that match the policy criteria.
2.  For each matching resource, the system updates Business hours reports showing spend during and outside business hours for the last 30 days.
3.  Based on the policy's approval type, the system generates change requests to enforce the on/off schedule. Business hours operations are directly integrated with the ServiceNow® Change Management feature. Either of the following change requests are generated:
    -   A change request for each resource that matches a policy.
    -   A single change request that applies to all CIs that match the policy.
4.  When a change request is approved, the system schedules on/off actions for the matching resources as specified in the policy.
5.  The process repeats each time billing data is updated.

**Note:** Azure supports compute resources only. Database resources aren't supported for Business hours on Azure.

**Important:** Provider-specific behavior:

AWS only: AWS Auto Scaling group \(ASG\) operations maintain minimum capacity for ASG-member resources. To avoid conflicts, the Cloud Cost Management application excludes all ASG-member instances from Business hours operations. You can view excluded resources on the **Excluded Resources** tab for Business hours.

Google Cloud only: Instances can be defined as Managed instance groups \(MIGs\), which run identical VMs across multiple zones with automated autoscaling, auto-healing, and automatic updating. VMs that are part of an MIG are excluded from Business Hours policies because MIGs automatically restart stopped instances.

## Cloud Cost Management recommendations for Business hours

Before scheduling on/off actions, Cloud Cost Management generates Business hours recommendations within ServiceNow. These recommendations surface in the Business hours reports and give you visibility into resources that are running outside their required hours, without requiring immediate action.

-   **Start with report-only**

    Use the Report-only approval type as a starting point for reviewing recommendations and validating your policy criteria before enabling automated scheduling. This enables you to assess potential savings and confirms resource matches before committing to on/off actions.

-   **Recommendation scope**

    Recommendations are scoped to resources discovered and tracked in the CMDB. Only resources that match your policy's provider, service account, and tag criteria appear in the reports. This ensures the Business hours recommendations reflect your actual managed cloud estate rather than all billing data.


## Business hours approval types

The approval type you select in a policy determines what actions the system takes for each resource that matches the policy criteria.

-   **Auto-approval \(Standard Change\) approval type**
    -   Generate a recommendation to apply the specified business hours and add the resource to the Business hours reports.
    -   Generate and then auto-approve a change request for the change group.
    -   Add the resource to the Business hours reports.
    -   Apply the Business hours schedule to the resource.
-   **Manual approval \(Normal Change\) approval type**
    -   Generate a recommendation to apply the specified business hours schedule and add the resource to the Business hours reports.
    -   Generate a change request for members of the change group.
    -   Add the resource to the Business hours reports.
    -   Any member of the group with the sn\_change\_write role can approve the change request.
    -   When approved, apply the Business hours schedule to the resource.
-   **Report-only approval type**
    -   Generate a recommendation to apply the specified business hours.
    -   Add the resource to the Business hours reports.

**Related topics**  


[Optimization view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/cloud-cost-management/optimization-view-ccm-ws.md)

[Define or update a Business hours policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/cloud-cost-management/bh-policy-create-cloudin.md)

[Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/c_ITILChangeManagement.md)

[Exclude a resource from all Cloud Cost Management reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/cloud-cost-management/exclusion-list-add-to-cloudin.md)

