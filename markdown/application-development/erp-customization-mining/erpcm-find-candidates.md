---
title: Save potential candidates to replatform
description: Use ERP Customization Mining \(ERP-CM\) to save ERP \(Enterprise Resource Planning\) app candidates to replatform.
locale: en-US
release: xanadu
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Finding and working with candidates to replatform, ERP Customization Mining \(ERP-CM\), Building low-code applications, Developing your application, Building applications]
---

# Save potential candidates to replatform

Use ERP Customization Mining \(ERP-CM\) to save ERP \(Enterprise Resource Planning\) app candidates to replatform.

## Before you begin

Admins must first configure the connection to the ERP system in ERP Data Hub. For more information, see [Working with ERP systems in ERP Data Hub](../../erp-integration/concept/erp-canvas-work-with-systems.md).

Role required: sn\_erp\_mining.erp\_user

## About this task

Candidates are custom applications in your ERP system. ERP-CM scans your system of record to build a profile based on application logs and database activity logs. ERP-CM also scans for custom applications based on customized namespaces and other criteria. Replatformed apps use the ERP system of record as the live data source.

**Note:**

If you delete a candidate from ERP-CM, it automatically reappears the next time the ERP system is scanned. Instead of deleting candidates, use the **Save as potential candidate** feature to organize your candidates.

## Procedure

1.  Navigate to **All** &gt; **ERP Foundation** &gt; **ERP Customization Mining**.

    ERP-CM accesses the remote table that calls the system of record instance, and temporarily mirrors that data in the ServiceNow AI Platform.

2.  Select the candidates icon \(![Candidates icon](../image/erpcm-candidates-icon.png)\) in the side panel.

3.  Select the candidate that you want to save as potential.

    Alternatively, you can select a candidate directly on the ERP-CM home page. For more information, see [Browse an overview of candidates in ERP-CM](erpcm-view-home-page-overview.md).

4.  Select the **Select as potential candidate** button.

    ![Save the potential candidate](../image/erpcm-save-potential-candidate.png)

    If you change your mind and want to remove the candidate from the potential candidates list, select the **Change to draft candidate** button.

    **Note:** The score improvement feature is available starting with Xanadu Store Release 2.


## Result

Selecting a candidate as a potential candidate changes the candidate status from Draft to Potential. The selected candidate is added to the Your selected potential candidates list on the home page.

## What to do next

After you identify candidates, use ERP Data Hub to view custom fields in remote and extraction tables, and add them to your ERP model. For more information, see [Building and managing ERP models to work with ERP data](../../erp-integration/concept/work-with-erp-data-models.md).

ERP-CM also recommends possible next steps for each candidate. For more information, see [Check candidate recommendations in ERP-CM](erpcm-work-with-recommendations.md).

**Parent Topic:**[Finding and working with candidates to replatform](../concept/work-with-candidates.md)

