---
title: Business hours
description: A Business Hours job applies policies to identify cloud resources that are running when they should be powered off. It reports those resources and starts or stops them on a schedule you define. Running resources during business hours only can help reduce your cloud spend.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/cloud-cost-management/bh-cloudin.html
release: brazil
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Explore, Cloud Cost Management, IT Asset Management, Asset Management]
---

# Business hours

A Business Hours job applies policies to identify cloud resources that are running when they should be powered off. It reports those resources and starts or stops them on a schedule you define. Running resources during business hours only can help reduce your cloud spend.

The insights\_admin role can create policies for AWS and GCP databases.

**Note:** Azure supports compute resources only. Database resources aren't supported for Business hours on Azure.

## How the Business hours feature works

Each successful Billing Download job triggers Business hours, along with the Budget forecast, Reservation plans, Rightsizing, and Unused resources, to analyze the spend and usage data. It also updates the actionable recommendations in the reports.

\[Omitted image "bh-policy-flow-diagram.png"\] Alt text: Process flow for Business hours

The Business hours process runs as follows:

1.  For each Business hours policy, the system queries the CMDB to identify resources that match the policy criteria.
2.  For each matching resource, the system updates Business hours reports showing spend during and outside business hours for the last 30 days.
3.  Based on the policy's approval type, the system generates change requests to enforce the on/off schedule. Business hours operations are directly integrated with the ServiceNow® Change Management feature. Either of the following change requests are generated:
    -   A change request for each resource that matches a policy.
    -   A single change request that applies to all CIs that match the policy.
4.  When a change request is approved, the system schedules on/off actions for the matching resources as specified in the policy.
5.  The process repeats each time billing data is updated.

**Important:** Provider-specific behavior

AWS only: AWS Auto Scaling group \(ASG\) operations maintain minimum capacity for ASG-member resources. To avoid conflicts, the Cloud Cost Management application excludes all ASG-member instances from Business hours operations. You can view excluded resources on the **Excluded Resources** tab for Business hours.

Google Cloud only: Instances can be defined as Managed instance groups \(MIGs\), which run identical VMs across multiple zones with automated autoscaling, auto-healing, and automatic updating. VMs that are part of an MIG are excluded from Business Hours policies because MIGs automatically restart stopped instances.

## Cloud Cost Management recommendations for Business hours

Before scheduling on/off actions, Cloud Cost Management generates Business hours recommendations natively within ServiceNow. These recommendations surface in the Business hours reports and give you visibility into resources that are running outside their required hours, without requiring you to take immediate action.

Use the Report-only approval type as a starting point for reviewing recommendations and validating your policy criteria before enabling automated scheduling. This enables you to assess potential savings and confirms resource matches before committing to on/off actions.

Recommendations are scoped to resources discovered and tracked in the CMDB. Only resources that match your policy's provider, service account, and tag criteria appear in the reports. This ensures the Business hours recommendations reflect your actual managed cloud estate rather than all billing data.

## Finance department Business hours policy

The following example shows a configured Business hours policy and its behavior.\[Omitted image "bh-policy-example.png"\] Alt text: Business Hours policy example

-   The policy is active, which is applied every time billing and usage data is updated.
-   The approval type is Manual approval \(Normal Change\), which means after a qualified user approves the change request, the schedule for resources that match the policy is adjusted.
-   The Business hours \(on/off\) schedule is **ON** from 8:00 a.m. to 5:00 p.m.
-   The power-on and power-off flows are specified.
-   Only resources that meet the following resource criteria match the policy:
    -   The cloud provider is `AWS` and the service account is `Billing 15970`.
    -   The resource has a tag with the name **Department** with the value `Finance`.

For each resource that matches this policy and where the change request is approved, the system starts the resource at 8:00 a.m. and stops it at 5:00 p.m.

**Note:** Actual start and stop times may vary slightly due to system demand and the time required for resources to start and stop.

## Business hours approval types

The approval type you select in a policy determines what actions the system takes for each resource that matches the policy criteria.

-   **Auto-approval \(Standard Change\) approval type**
    -   Generates a recommendation to apply the specified business hours and add the resource to the Business hours reports.
    -   Generates and then auto-approves a change request for the change group.
    -   Adds the resource to the Business hours reports.
    -   Applies the Business hours schedule to the resource.
-   **Manual approval \(Normal Change\) approval type**
    -   Generates a recommendation to apply the specified business hours schedule and add the resource to the Business hours reports.
    -   Generates a change request for members of the change group.
    -   Adds the resource to the Business hours reports.
    -   Any member of the group with the sn\_change\_write role can approve the change request.
    -   When approved, applies the Business hours schedule to the resource.
-   **Report-only approval type**
    -   Generates a recommendation to apply the specified business hours.
    -   Adds the resource to the Business hours reports.

**Related topics**  


[Define or update a Business hours policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/cloud-cost-management/bh-policy-create-cloudin.md)

[Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/c_ITILChangeManagement.md)

[Exclude a resource from all Cloud Cost Management reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/cloud-cost-management/exclusion-list-add-to-cloudin.md)

