---
title: Business hours
description: A Business hours job applies policies to identify resources that are running when they should be powered off, reports them, and can start and stop them on a schedule that you specify. Running only during specified business hours can significantly reduce your cloud spend.
locale: en-US
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Exploring Cloud Cost Management, Cloud Cost Management, IT Asset Management]
---

# Business hours

A Business hours job applies policies to identify resources that are running when they should be powered off, reports them, and can start and stop them on a schedule that you specify. Running only during specified business hours can significantly reduce your cloud spend.

The insights\_admin role can create policies for AWS and GCP databases.

**Note:** Azure only supports compute, not database.

## How the Business hours feature works

Each successful execution of a Billing Download job triggers the Budget Forecast, Business Hours, Reservation Plans, Rightsizing, and Unused resources jobs to analyze the spend and usage data and to update the actionable recommendations in the reports. Business Hours jobs follow this process.

![Process flow for Business Hours](../image/bh-policy-flow-diagram.png "How the Business Hours feature works")

1.  For each Business hours policy, examine the CMDB to identify resources that match the policy criteria.
2.  For each resource that matches a policy, update Business hours reports that show spend for business hours and non-business hours usage for the last 30 days.
3.  Business hours operations are directly integrated with the ServiceNow® Change Management feature. For Manual Approval or Auto-approval policy types, generate change requests to enforce the on/off schedule that is defined in the policy. Either of the following, depending on policy settings:
    -   Generate a change request for each resource that matches a policy.
    -   Generate a single change request that applies to all CIs that match the policy.
4.  When a change request is approved, schedule the on/off actions for the associated resources as specified in the policy.
5.  Repeat the process whenever billing data is updated.

**Important:**

AWS only:

-   AWS Auto Scaling group \(ASG\) operations act to maintain minimum capacity for ASG-member resources. To avoid conflicts with ASG operations, the Cloud Cost Management app excludes all instances that are part of an Auto Scaling group from Business Hours operations.
-   You can view ASG-member resources on the **Excluded Resources** tab for Business Hours.

Google Cloud only: The instance can be defined as a Managed instance groups \(MIGs\). MIGs let you operate applications on multiple identical VMs. You can make your workloads scalable and highly available by taking advantage of automated MIG services, including: auto-scaling, auto-healing, regional \(multiple zone\) deployment, and automatic updating.

## Business hours policy

![Business Hours policy example](../image/bh-policy-example.png)

The Finance department policy example has the following settings:

-   The policy is active, which is applied every time billing and usage data is updated.
-   The approval type is Manual approval \(Normal Change\), which means that, after a qualified user approves the change request, the schedule for resources that match the policy is adjusted.
-   The Business hours \(on/off\) schedule is **ON** from 8:00 AM to 5:00 PM.
-   The power-on and power-off flows are specified.
-   Only resources that meet the following resource criteria match the policy:
    -   The cloud provider is `AWS` and the service account is `Billing 15970`.
    -   The resource has a tag with the name **Department** with the value `Finance`.

After the policy is applied, for each resource that matches the policy and where the change request was approved, the system starts the resource at 8:00AM and stops it at 5:00PM. The actual start and stop times vary slightly due to changes in system demand and the time that it takes for the resource to start and stop.

![Result of the example Business Hours policy](../image/policy-illustration.png)

## Business hours approval types

For each resource that matches the policy criteria, the actions that the policy takes depend on the approval type:

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


[Define or update a Business hours policy](../task/bh-policy-create-cloudin.md)

[Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/c_ITILChangeManagement.md)

[Exclude a resource from all Cloud Cost Management reports](../task/exclusion-list-add-to-cloudin.md)

