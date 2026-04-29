---
title: Monitor the plan list and generate the PDF
description: Monitor the list of the business continuity plans \(BCPs\) in the BCM mobile application. You can save and generate the PDF of a plan record.
locale: en-US
release: australia
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing plans with BCM mobile application, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Monitor the plan list and generate the PDF

Monitor the list of the business continuity plans \(BCPs\) in the BCM mobile application. You can save and generate the PDF of a plan record.

## Before you begin

Role required: sn\_bcp.plan\_manager, sn\_bcp.plan\_viewer

## About this task

If you have the Business Continuity Management \(BCM\) plan program manager, BCM program manager, BCM plan manager, BCM Plan Viewer, or BCM plan contributor role, you can view the plan list icon in the BCM mobile application. On accessing the icon, you can view a list of approved plans.

To access the plan list screen, both the BCM mobile application and the BCM planning application must be installed.

## Procedure

1.  Navigate to the business continuity plans \(BCPs\) list view in the mobile app.

    In the BCM mobile application, the plan list screen is displayed to the users. The BCP plan viewer has access to the plans list when they’re logged in to the instance through an agent.

    ![Mobile app.](../image/mobile-plan-list.png)

    An instance can have the BCM mobile application as the only ServiceNow Agent application. When multiple ServiceNow Agent applications are available, the BCP plan viewer selects the BCM mobile application from the list and navigates to the plans. A list of the approved plans is displayed.

    To access each of these plans, the BCP plan viewer can select the plans one by one.

2.  Tap a plan record and view its details.

3.  To generate the PDF of the plan, tap the record, tap the **More** icon \(⋮\), and tap **Generate PDF**.

    You can generate the PDF of the plan by tapping the **Generate PDF** UI action.

    ![PDF.](../image/mobile-generate-pdf.png)

    The PDF is generated and a message is displayed that the selected plan PDF has been successfully generated for download.

4.  To save a particular plan, tap the **Save** icon in the top toolbar in the plan view, provide a name for the plan in the 'Save the item' dialog box, and tap **Done**.

    The Save functionality is provided as part of the base version.

    The PDF of the selected plan is saved in the instance. Similarly, as a plan manager or plan viewer, you can view all saved records in the **Saved items** tab of the app.

    ![Saved items.](../image/mobile-saved-tems-tab.png)


