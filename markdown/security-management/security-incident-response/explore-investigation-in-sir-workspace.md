---
title: Explore Investigation Canvas
description: The primary objective of the investigation canvas is to present the necessary security incident data in one common place.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Investigation Canvas, SIR Workspace Orchestration, Working with Security Incident Records, Use, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Explore Investigation Canvas

The primary objective of the investigation canvas is to present the necessary security incident data in one common place.

Within the SIR Workspace, the security incident investigation primarily revolves around a few key entry points.

The following are a few key entry points that are provisioned for the security analysts within the base system:

-   Associated Observables
-   Configuration Items
-   Affected Users
-   Associated Phish Emails
-   Email Search

You can also configure entry points by adding, modifying, or removing the entry points. For more information, see [Configure SI design time investigation](configure-investigation-canvas-records.md).

On the **Investigation** tab, the entry point table acts as the parent table. All the tables that hold the results of an orchestration action performed on the parent table are presented as children table within the entry point.

For example, for **Associated Observables** entry point, **Associate Observables** table is the parent table, and other tables such as Threat Lookup Results, Sandbox submission results are the children tables.

The security analyst can perform all the orchestration actions on the Associated Observables table, and is able to view all the associated information within the same page, without the need to navigate across multiple places.

**Note:** Select the interactable charts on the **Overview** page, such as malicious observables, to see the filtered view of malicious observables within the investigation canvas. Alternatively, you can directly begin the investigation by navigating to the investigation canvas, which has all the data.

The **Investigation** tab provides you a work notes field to add any comments and post it. You can also use the **Email** option, to send email to the necessary stakeholders.

The list of children table under an entry point is also configurable. For more information, see [Configure SI design time investigation](configure-investigation-canvas-records.md).

The following is a detailed example of an entry point \(Associated Observable\) that are configured and provisioned within the base system:

1.  Select the **Associated Observables** entry point from the drop-down list.

    Here the parent table is also **Associated Observable**.

    ![Entry points](../image/entry-points.png "Entry Point List Configs")

2.  Select one or more observables from the parent table.
3.  Run the desired capability.

    For example, select **Run Threat Lookup** to fetch the threat lookup results for a selected observable.

    **Note:** When a corresponding observable action is executed, the process is run in the backend and the results are displayed below the Observables list.

4.  Select **View Associated Info** to view the observables results. The results are displayed on the same page.

    **Note:** You can view the results using filters by results, select either **All results** or **Latest Results**. By default, the latest results are displayed. If there are multiple implementations \(of integrations\), then the latest results according to the implementation are shown.

    In addition, you can filter the results **by associated related lists** which are the children table results. By default, all the configured children table related lists are displayed. For more information, see [Configure SI design time investigation](configure-investigation-canvas-records.md). However, you can choose to select only those children tables that are required.

    ![View associated info.](../image/sirw-explore-investigation-view-info.png)

5.  Select **View Associated Info** to view all the associated children table data in one place. However you can close the related lists view by selecting **Close View** button. Once you close the view, you can only see the observables parent table as earlier.
6.  Select **Expand all** upward direction icon within the **Viewing available associated info** results table to expand all the related lists children table data.

    ![Expand all option view.](../image/sirw-expanded-view-associated-info-observables.png)

7.  Select **Collapse all** downward direction icon to collapse all the related lists children table data.

    **Note:** The banner on top of the associated info section that contains all the children table data shows how many observable related information is presented to the user. For example, initially if you select two observables and select **View Associated Info**, the banner shows, **Viewing available associated info for 2 Associated Observables.**. If you select one more observable, the banner says that the information is outdated. Select **View Associated Info** again to fetch the latest data.

    ![Associated observables results outdated](../image/outdated-info.png)

    Select the observable to open the parent table record form in a different tab with a more detailed view of the selected record. All the associated children table data of that particular selected record is also presented under the **Associated info** section.

    However, the associated info section displays only the latest results of the children table, as seen in the investigation canvas, in the read-only mode. No actions are possible in this view. The form page of the children table can be opened in a new tab that renders the fully functional page with any actions, if any.

    You can switch between the different tables using the drop-down list. You can also expand or collapse each form under the associated info section.

    Within the **Observable** form page \(parent table record form page\) you can perform certain actions as available. Whenever you perform an action, select refresh on the associated info banner to refresh the data.

8.  Select **Expand all** to expand all the related lists children table. By default, all the children are expanded.

    ![Entry point expanded view](../image/expand-all-info.png "Expanded view of the observables")


**Parent Topic:**[SIR Workspace Investigation Canvas](security-incident-response-investigation-canvas.md)

**Related topics**  


[Configure SI design time investigation](configure-investigation-canvas-records.md)

