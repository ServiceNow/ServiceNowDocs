---
title: Finding and working with candidates to replatform
description: Use ERP Semantic Mining \(ERP-CM\) to identify potential ERP \(Enterprise Resource Planning\) app candidates for replatforming.
locale: en-US
release: yokohama
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [ERP Semantic Mining \(ERP-CM\), Building low-code applications, Developing your application, Building applications]
---

# Finding and working with candidates to replatform

Use ERP Semantic Mining \(ERP-CM\) to identify potential ERP \(Enterprise Resource Planning\) app candidates for replatforming.

Replatforming is the process of scanning legacy ERP system code to find potential candidates to move onto your ServiceNow AI Platform instance as new apps. You can use data from the ERP system as a source for apps built on the ServiceNow AI Platform, improving performance, enhancing security, and reducing maintenance.

ERP Semantic Mining evaluates application candidates and presents a numeric score. The higher the score, the better the candidate is for replatforming.

-   A high potential indicates that ERP-CM can immediately use remote tables and extraction tables that match the ERP model for the application candidate without making additional changes.
-   A low potential indicates that the application candidate matches few of the remote tables and extraction tables in the ERP models in Zero Copy Connector for ERP.

Good candidates for replatforming tend to be smaller applications that use data from the system of record.

**Note:**

If you delete a candidate from ERP-CM, it automatically reappears the next time the ERP system is scanned. Instead of deleting candidates, use the **Save as potential candidate** feature to organize your candidates.

If ERP-CM shows that a candidate has a number of similar candidates, consider building one app that meets the needs of some or all similar candidates when you replatform.

-   **[Obtaining ERP Semantic Mining statistics and mining analysis](erpcm-obtaining-statistics-and-mining-analysis.md)**  
Use the ERP Semantic Mining home page dashboard to obtain statistics about candidates and info to help you troubleshoot.
-   **[Browse an overview of candidates in ERP-CM](../task/erpcm-view-home-page-overview.md)**  
View the ERP Semantic Mining \(ERP-CM\) home page for a summary of ERP \(Enterprise Resource Planning\) app candidates to replatform onto the ServiceNow AI Platform.
-   **[View and work with candidate details in ERP-CM](../task/erpcm-view-work-with-candidate-details.md)**  
View and edit candidate details and recommended actions in ERP Semantic Mining \(ERP-CM\). Analyze ERP \(Enterprise Resource Planning\) system scan results, linked ERP models, usage, and similar candidates.
-   **[Check candidate recommendations in ERP-CM](../task/erpcm-work-with-recommendations.md)**  
Check the actions that ERP Semantic Mining \(ERP-CM\) suggests to improve the ease of replatforming an ERP \(Enterprise Resource Planning\) candidate.
-   **[Save potential candidates to replatform](../task/erpcm-find-candidates.md)**  
Use ERP Semantic Mining \(ERP-CM\) to save ERP \(Enterprise Resource Planning\) app candidates to replatform.

**Parent Topic:**[ERP Semantic Mining \(ERP-CM\)](erp-customization-mining-overview.md)

