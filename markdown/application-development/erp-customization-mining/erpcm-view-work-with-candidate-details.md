---
title: View and work with candidate details in ERP-CM
description: View and edit candidate details and recommended actions in ERP Customization Mining \(ERP-CM\). Analyze ERP \(Enterprise Resource Planning\) system scan results, linked ERP models, usage, and similar candidates.
locale: en-US
release: xanadu
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Finding and working with candidates to replatform, ERP Customization Mining \(ERP-CM\), Building low-code applications, Developing your application, Building applications]
---

# View and work with candidate details in ERP-CM

View and edit candidate details and recommended actions in ERP Customization Mining \(ERP-CM\). Analyze ERP \(Enterprise Resource Planning\) system scan results, linked ERP models, usage, and similar candidates.

## Before you begin

Role required: sn\_erp\_mining.erp\_user

## Procedure

1.  Navigate to **All** &gt; **ERP Foundation** &gt; **ERP Customization Mining**.

2.  In the side panel, select the candidates icon \(![Candidates icon](../image/erpcm-candidates-icon.png)\).

3.  View and edit the basic details for a candidate in a new tab within ERP-CM by selecting the candidate **Name** in the candidates list.

    Alternatively, you can select a candidate directly on the ERP-CM home page. For more information, see [Browse an overview of candidates in ERP-CM](erpcm-view-home-page-overview.md).

    The **Details** tab of the candidate is where you can review and update any basic details, as well as work with comments, attachments, and the Activity stream.

<table id="table_g5l_wp4_jyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Record number of the potential candidate, which is automatically generated.

</td></tr><tr><td>

Status

</td><td>

Status of the candidate, either **Draft** or **Potential**.When you evaluate a draft candidate and decide the candidate is good to replatform, you can change the status from **Draft** to **Potential**.

</td></tr><tr><td>

ERP application

</td><td>

Name of the ERP application on the ERP system.

</td></tr><tr><td>

ERP module

</td><td>

Functional business area of the ERP system, such as **Sales**.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the candidate, what the application does.

</td></tr><tr><td>

Long text

</td><td>

Additional information about the candidate.

</td></tr></tbody>
</table>4.  Work with the next recommended steps by selecting the **Recommendations** tab.

    For more information, see [Check candidate recommendations in ERP-CM](erpcm-work-with-recommendations.md).

5.  View details on which tables were relevant to the candidate and the details of their scan on the ERP system by selecting the **ERP scan results** tab.

    For a description of the field values, see [ERP-CM candidate scan results field descriptions](../reference/erpcm-candidate-scan-results-descriptions.md).

    ![ERP-CM scan results](../image/erpcm-candidate-scan.png "Candidate scan results")

6.  Check and note which ERP models are ERP-CM identified as being related to the candidate by selecting the **Models** tab.

    |Field|Description|
    |-----|-----------|
    |Model type|ERP model relevant to the candidate. This model can be a standard ERP model \(which you work with in ERP Data Hub\), a workflow, or a custom business area.|
    |Relevant for implementation|Whether the ERP model is required for replatforming.|
    |Module|ERP business area for the model on the system of record, such as **Sales**.|
    |Table names|Names of the tables in the ERP model on the ERP system.|
    |Updated|Date and time the list was most recently updated.|

    You can note which ERP models to work with in ERP Data Hub.

7.  Check the number of system users that use the candidate application by selecting the **Usage** tab.

8.  Research candidates related to the current candidate and their tables by selecting the **Similar candidates** tab.

    Similar candidates are helpful when planning how to best replatform a legacy app. When you replatform a custom app from the system of record, you don't have to replicate the old app exactly. Use the replatforming process to design a better app, perhaps one that addresses the needs of multiple similar candidates in a single, new app built using low-code tools on the ServiceNow AI Platform.

    For a description of the field values, see [ERP-CM similar candidates field descriptions](../reference/erpcm-similar-candidates-field-descriptions.md).

9.  Select the **Save** button and save any changes you made to the candidate details.


## What to do next

After you work with the candidate details and identify similar candidates, you can:

-   [Check candidate recommendations in ERP-CM](erpcm-work-with-recommendations.md).
-   [Save potential candidates to replatform](erpcm-find-candidates.md).
-   Continue building remote table and extraction tables in the relevant ERP model in ERP Data Hub, making the data available on the ServiceNow AI Platform. For more information, see [Using ERP models, extraction tables, and remote tables](../../erp-integration/concept/work-with-erp-systems-connections-and-remote-tables.md).

**Note:**

If you delete a candidate from ERP-CM, it automatically reappears the next time the ERP system is scanned. Instead of deleting candidates, use the **Save as potential candidate** feature to organize your candidates.

**Parent Topic:**[Finding and working with candidates to replatform](../concept/work-with-candidates.md)

