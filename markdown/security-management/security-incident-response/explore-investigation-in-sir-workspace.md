---
title: Explore Investigation Canvas
description: The primary objective of the investigation canvas is to present the necessary security incident data in one common place.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [SIR Workspace Investigation Canvas, SIR Workspace Orchestration, Working with Security Incident Records, Using SIR Workspace, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
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

You can also configure the above entry points by adding or modifying or removing the entry points as applicable. For more information, see [Configure SI design time investigation](configure-investigation-canvas-records.md).

On the **Investigation** tab, the entry point table acts as the parent table. All the tables that hold the results of an orchestration action performed on the parent table are presented as children table within the entry point.

For example, for **Associated Observables** entry point, **Associate Observables** table is the parent table, and other tables such as Threat Lookup Results, Sandbox submission results, and so on are the children table.

The Security Analyst can perform all the orchestration actions on the Associated Observables table, and will be able to view all the associated information within the same page, without the need to navigate across multiple places.

**Note:** When a user clicks on the interactable charts on the **Overview** page such as malicious observables, the user will be navigated to the filtered view of malicious observables within the investigation canvas. Alternatively, the user can directly begin the investigation by navigating to the investigation canvas which will have all the data.

The list of children table under an entry point is also configurable. For more information, see [Configure SI design time investigation](configure-investigation-canvas-records.md).

The following is a detailed example of an entry point \(Associated Observable\) that are configured and provisioned within the base system:

1.  Select the **Associated Observables** entry point from the drop down list.

    Here the parent table is also **Associated Observable**.

    ![Entry points](../image/entry-points.png "Entry Point List Configs")

2.  Select one or more observables from the parent table.
3.  Run the desired capability.

    For example, select **Run Threat Lookup** to fetch the threat lookup results for a selected observable.

    **Note:** When a corresponding observable action is executed, the process is run in the backend and the results are displayed below the Observables list.

4.  Click **View Associated Info** to view the observables results. The results are displayed on the same page.

    **Note:** You can view the results using filters by results, select either **All results** or **Latest Results**, whichever is the desired view. By default, the latest results are displayed. If there are multiple implementations \(of integrations\), then latest results per implementation will be shown.

    In addition, you can filter the results **by associated related lists** which are the children table results. By default, all the configured children table related lists are displayed. For more information, see [Configure SI design time investigation](configure-investigation-canvas-records.md). However, you can choose to select only those children tables that are required.

    ![View associated info.](../image/sirw-explore-investigation-view-info.png)

5.  By clicking **View Associated Info** you can view all the associated children table data in one place, however you can close the related lists view by selecting **Close View** button. Once you close the view, you can only see the observables parent table as earlier.
6.  Click **Expand all** upward direction icon within the **Viewing available associated info** results table to expand all the related lists children table data.

    ![Expand all option view.](../image/sirw-expanded-view-associated-info-observables.png)

7.  Click **Collapse all** downward direction icon to collapse all the related lists children table data.

    **Note:** The banner on top of the associated info section that contains all the children table data shows how many observable related information is being presented to the user. For example, initially if you select two observables and click **View Associated Info**, the banner shows, **Viewing available associated info for 2 Associated Observables.**. If you select for example, another observable, the banner says that the information is outdated \(screenshot below\). You will have to click **View Associated Info** again to get the latest data.

    ![Associated observables results outdated](../image/outdated-info.png)

    In addition to the above comprehensive view of the Observables associated information, if you would want to view more information about a record on the parent table then click the observable and the parent table record form opens in a different tab with a more detailed view of the selected record. All the associated children table data of that particular selected record is also presented under the **Associated info** section.

    However, the associated info section displays only the latest results of the children table, as seen in the investigation canvas, in the read-only mode. No actions are possible in this view. The form page of the children table can be opened in a new tab that will render the fully functional page with any actions, if any.

    You can switch between the different tables using the drop-down list. You can also expand or collapse each form under the associated info section.

    Within the **Observable** form page \(parent table record form page\) you can perform certain actions as available. Whenever you perform an action, you can click refresh on the associated info banner to refresh the data.

8.  Click **Expand all** to expand all the related lists children table. By default, all the children are expanded.

    ![Entry point expanded view](../image/expand-all-info.png "Expanded view of the observables")


**Parent Topic:**[SIR Workspace Investigation Canvas](security-incident-response-investigation-canvas.md)

**Related topics**  


[Configure SI design time investigation](configure-investigation-canvas-records.md)

