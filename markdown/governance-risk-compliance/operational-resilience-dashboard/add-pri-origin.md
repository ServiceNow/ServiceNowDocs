---
title: Add the primary origin
description: Add a primary origin of an operational vulnerability in its record. Once the primary origin of the operational vulnerability is specified, its upstream dependencies are automatically included in the impacted areas. It enables you to view the operational vulnerability from all affected perspectives. The source is automatically added as the primary origin on the Primary origin tab.
locale: en-US
release: australia
product: Operational Resilience Dashboard
classification: operational-resilience-dashboard
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Managing Operational vulnerability, Managing Operational Resilience, Operational Resilience, Governance, Risk, and Compliance]
---

# Add the primary origin

Add a primary origin of an operational vulnerability in its record. Once the primary origin of the operational vulnerability is specified, its upstream dependencies are automatically included in the impacted areas. It enables you to view the operational vulnerability from all affected perspectives. The source is automatically added as the primary origin on the **Primary origin** tab.

## Before you begin

Role required: Analyst assigned to the operational vulnerability

## About this task

Beginning with Release 20.1.x, the Operational Resilience application supports the latest Common Service Data Model \(CSDM\). The enhanced functionality supports the roll up of the dependencies.

Consider the following example where the relationships are configured between objects.

![CSDM objects.](../image/csdm-objects-rel.png)

If you have a business process BP1 as shown in the relationship diagram, it has service offering SO1 and business service BS1 as upstream relationships. With the enhanced functionality, adding BP1 as an operational vulnerability automatically includes SO1 and BS1 in the impacted areas, which are displayed in the Impacted Areas tab of the operational vulnerability record.

## Procedure

1.  Navigate to **Workspaces** &gt; **Operational Resilience Workspace** &gt; **All Operational Vulnerabilities**.

2.  Open the vulnerability for which you want to add the related area.

3.  Update the source in the **Source** field.

4.  Update the source record in the **Source record** field in the Primary origin section of the **Details** tab and select **Save**.

    If you add the source in the **Source** field and the source record in the **Source record** field in the Primary origin section of the **Details** tab, the system automatically edits the primary origin and displays it on the **Primary origin** tab. In the following example, the Source Table is Business Service, the Source is Business service, and the selected source record is BS1000.![Source field.](../image/pri-origin-src-field.png)

    As shown in the example, the source record BS1000 is automatically updated as the primary origin on the **Primary origin** tab.![Primary origin tab.](../image/pri-origin-updated.png)

    Adding the primary origin automatically adds its upstream dependencies to the impacted areas as shown in the example. The operational vulnerability can be seen from all the impacted area.

    ![Primary origin impacted area.](../image/pri-ori-imp-area.png)

    For example, you establish a relationship from a business service to a service offering, and from the service offering to a business process \(BS - SO - BP\), where SO is the downstream entity of BS and BP is the downstream entity of SO. In the **Primary origin** tab of the operational vulnerability, if you fetch the business process \(BP\), it automatically adds its upstream dependencies, as shown in the examples.

    ![Dependency.](../image/pri-ori-up-dep-1.png)![Upstream dependencies.](../image/pri-ori-up-dep-2.png)

    **Note:** When the scheduled job is run, the operational vulnerabilities are gathered and shown in the red flags section of the Home page.

5.  On the **Primary origin** tab, select **Add**.

    You can add the primary origin of the operational vulnerability.

    ![Primary origin added.](../image/op-vul-pri-ori.png)

    When you add the primary origin of the operational vulnerability, its impacted areas with upstream entities are updated on the **Impacted areas** tab.

    When the **Calculate red flags for CSDM and dependencies** scheduled job is executed, the updated impacted areas and the operational vulnerability count are updated on the dashboard.

    ![Count 0.](../image/op-vul-count-0.png)

    For example, when the impacted areas in the operational vulnerability are updated, the operational vulnerability count on the overview page of SO1 is 0 before the scheduled job runs. After running the scheduled job, the operational vulnerability count on the overview page of SO1 is updated to 1. This ensures that the updated data is promptly reflected on the Operational Resilience dashboard.

    ![Count 1.](../image/op-vul-count-1.png)

6.  To update the impacted areas for a primary origin of the operational vulnerability, select **Updated impacted area**.

    The application fetches the impacted areas for the primary origin.

7.  To view the status of the uploaded upstream assets of the primary origin, select the **View progress** UI action.

    The Operational Resilience administrator or manager can view the progress when adding the impacted assets to the operational vulnerabilities. The assets are listed in the **Impacted areas** tab as shown in the example.

    ![Impacted areas.](../image/op-vul-pri-ori-view-progress.png)


