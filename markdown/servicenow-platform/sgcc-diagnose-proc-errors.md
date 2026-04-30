---
title: Diagnose a processing error in SGC Central
description: Diagnose processing errors in connections configured for a Service Graph Connector and resolve them within the SGC Central view of the Service Graph Workspace or CMDB Workspace using recommendations from Now Assist.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-06"
reading_time_minutes: 1
breadcrumb: [Managing connections, SGC Central, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Diagnose a processing error in SGC Central

Diagnose processing errors in connections configured for a Service Graph Connector and resolve them within the SGC Central view of the Service Graph Workspace or CMDB Workspace using recommendations from Now Assist.

## Before you begin

Verify that the Service Graph Connector diagnosis skill is enabled. For more information, see [Configure the Service Graph Connector diagnosis skill](../../configuration-management/task/now-assist-cmdb-config-sgc-diagnose.md).

Role required: SGC-admin or admin

## Procedure

1.  Use one of the following methods to open SGC Central:

    -   Navigate to **Workspaces** &gt; **Service Graph Workspace**, and from the left navigation panel, select the Ingestion icon to open the SGC Central view.
    -   Navigate to **Workspaces** &gt; **CMDB Workspace** &gt; **SGC Central**.
2.  On the Overview page, select the **Processing status** card.

    **Note:** On the **Processing status** card, only import sets with errors in the last import execution are counted as processing errors, and their count is displayed. However, the Error column in the summary table, which displays more details about the processing status, also includes canceled import sets. As a result, the error count on the Processing status card might not match the number of errors displayed in the summary table.

3.  When an error count is displayed on the **Processing status** card, select the **View details** link from the error summary for the connection.

4.  On the **Errors** tab, select an error for a failed import set.

    **Note:** You can diagnose only one error at a time. The **Diagnose Error** button is enabled only when you select an error from the list.

    ![Errors tab showing the Diagnose error button that is displayed after selecting an error.](../image/sgcc-diagnose-error.png "Diagnose a processing error")

5.  Select **Diagnose error**.


## Result

Now Assist triggers the diagnosis process for the processing error. The Error diagnosis window includes two key sections: Explanation and Recommendation, each focused on explaining the error and providing a solution to resolve it. The recommendation is based on a knowledge article matched using AI Search. A link to the knowledge article is provided in the Source section for additional guidance.

![Error diagnosis result for a processing error, showing the error explanation, a recommendation to resolve the error, and a link to the knowledge article as the source of the recommendation.](../image/sgcc-error-diagnosis.png "Error diagnosis result")

