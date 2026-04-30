---
title: Exploring ERP Semantic Mining
description: ERP Semantic Mining enables you to identify candidates for replatforming. These candidates can be custom applications that were built on legacy ERP \(Enterprise Resource Planning\) systems that you want to quickly replatform.
locale: en-US
release: zurich
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [ERP Semantic Mining overview, Workflow Data Fabric]
---

# Exploring ERP Semantic Mining

ERP Semantic Mining enables you to identify candidates for replatforming. These candidates can be custom applications that were built on legacy ERP \(Enterprise Resource Planning\) systems that you want to quickly replatform.

**Important:** Starting with the Zurich release, ERP Semantic Mining is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

## Identifying candidates to replatform with ERP Semantic Mining

Legacy ERP systems can contain old tables with custom fields that are difficult to maintain. Use Zero Copy Connector for ERP and ERP Semantic Mining to identify candidates with custom fields to extract onto their instance as remote tables or extraction tables. Low-code developers can then use the legacy ERP fields as data sources for apps created on the ServiceNow AI Platform, using a builder such as ServiceNow Studio, to replatform them.

You can use a combination of remote tables and extraction tables to retrieve data from your legacy ERP system.

-   Remote tables get their records from running an associated script against an external data source.
-   Extraction tables retrieve large amounts of data using a scheduled query, and use transform tables to process data for use on the ServiceNow AI Platform.

Replatforming is the process of scanning legacy ERP system code to find potential candidates to move onto your ServiceNow AI Platform instance as new apps. You can use data from the ERP system as a source for apps built on the ServiceNow AI Platform, improving performance, enhancing security, and reducing maintenance.

When you find ERP candidates to replatform, ERP Semantic Mining also provides suggestions for next actions and similar candidates. ERP Semantic Mining supports any ERP modules, or functional areas that admins configure in Zero Copy Connector for ERP. Some example modules are Finance, Procurement, and Sales. For more information, see [Building and managing models to work with ERP data](../../erp-integration/concept/work-with-erp-data-models.md).

Replatformed data is immediately available, mirrored in easy-to-manage tables and apps. Users no longer must request information from database administrators, which can take weeks. Replatformed apps use the ERP system of record as the live data source.

## Workflow for replatforming customized ERP applications

Complete the following workflow to replatform legacy ERP data with custom code from the system of record. All the work is done on the ServiceNow AI Platform using ERP Semantic Mining.

1.  Run an analysis with ERP Semantic Mining on the ERP system of record.
2.  Connect the ERP system of record to the ServiceNow instance with Zero Copy Connector for ERP.

    ERP Semantic Mining uses the system connections configured in Zero Copy Connector for ERP. For more information, see [Working with ERP systems in Zero Copy Connector for ERP](../../erp-integration/concept/erp-canvas-work-with-systems.md).

3.  Use Zero Copy Connector for ERP to build ERP models from fields on the available remote tables. For more information, see the following topics:
    -   [Building and managing models to work with ERP data](../../erp-integration/concept/work-with-erp-data-models.md)
    -   [Using ERP remote tables in Zero Copy Connector for ERP](../../erp-integration/concept/erp-canvas-work-with-remote-tables.md)
4.  Run ERP Semantic Mining to find candidates. Candidates are custom code in the system of record that you can replace with ServiceNow apps. For more information, see [Browse an overview of candidates in ERP Semantic Mining](../task/erpcm-view-home-page-overview.md).
5.  Choose the candidate to replatform. For more information, see [Save potential candidates to replatform](../task/erpcm-find-candidates.md).
6.  Use the candidate details in ERP Semantic Mining as a central place to enter comments and save attachments relating to the candidate. For more information, see [View and work with candidate details in ERP Semantic Mining](../task/erpcm-view-work-with-candidate-details.md).
7.  In the candidate details, identify any similar candidates that you could combine into a single replatformed app. For more information, see [Determining candidate score and potential](erpcm-potential-and-recommendations.md).
8.  Return to Zero Copy Connector for ERP to continue building data models with remote tables and extraction tables. Confirm that all the necessary data is available in the ServiceNow AI Platform. For more information, see [Building and managing models to work with ERP data](../../erp-integration/concept/work-with-erp-data-models.md).
9.  In ServiceNow Studio or another ServiceNow application, build a scoped app by using the replatformed data as a source. For more information, see [ServiceNow Studio](https://www.servicenow.com/docs/access?context=servicenow-studio-landing&version=zurich&pubname=zurich-application-development&ft:locale=en-US).
10. Measure and monitor the performance of the new app using applicable metrics and parameters with your preferred analytic tools.

## Benefits of ERP Semantic Mining

|Benefit|Feature|Role|
|-------|-------|----|
|Quickly identify candidates with custom code to replatform without waiting for your ERP administrator|[Save potential candidates to replatform](../task/erpcm-find-candidates.md)|sn\_erp\_mining.erp\_admin, sn\_erp\_mining.erp\_user|
|View suggestions for next steps and actions to guide you in replatforming|[Check candidate recommendations in ERP Semantic Mining](../task/erpcm-work-with-recommendations.md)|sn\_erp\_mining.erp\_admin, sn\_erp\_mining.erp\_user|
|Compile selected candidates in a list by saving them|[Save potential candidates to replatform](../task/erpcm-find-candidates.md)|sn\_erp\_mining.erp\_admin, sn\_erp\_mining.erp\_user|

## Additional resources for ERP Semantic Mining

<table id="table_flh_vjt_gtb"><thead><tr><th>

Learn more about ERP Semantic Mining

</th><th>

ServiceNow resources

</th></tr></thead><tbody><tr><td rowspan="3">

ERP Semantic Mining enables you to find application candidates with customized code in your ERP system.

</td><td>

![](../../../reuse/icons/brand-icons/bus-whitepaper.svg) [App Engine for ERP Overview on ServiceNow University](https://learning.servicenow.com/lxp/en/app-engine/enterprise-resource-planning-clean-core-with-app-engine-overview?id=learning_course_prev&course_id=ee84d77293bc35903cc0322d6cba10eb)

 **Note:** You must log in to ServiceNow University to access this resource.

</td></tr><tr><td>

![](../../../reuse/icons/brand-icons/bus-3-person.svg) [ServiceNow Community site](https://www.servicenow.com/community/?id=community_search&q=erp%20customization%20mining&spa=1)

</td></tr><tr><td>

![](../../../reuse/icons/brand-icons/bus-application-developer.svg) [Video: Unlock the full potential of your ERP system](https://www.youtube.com/watch?v=R66HqYLfEc8)

</td></tr></tbody>
</table>-   **[How ERP Semantic Mining extracts and processes data](how-erp-clean-core-inputs-data.md)**  
ERP Semantic Mining retrieves data from the ERP \(Enterprise Resource Planning\) system using extractors and processes it before the data is available on the ServiceNow AI Platform.
-   **[Determining candidate score and potential](erpcm-potential-and-recommendations.md)**  
ERP Semantic Mining generates a score to rank the potential for replatforming legacy ERP \(Enterprise Resource Planning\) candidates onto the ServiceNow AI Platform.
-   **[How ERP Semantic Mining works with Zero Copy Connector for ERP and remote tables](ecm-and-erp-integration.md)**  
Zero Copy Connector for ERP enables you to connect to your ERP \(Enterprise Resource Planning\) system of record, and to organize its data.
-   **[Recommendations and similar candidates in ERP Semantic Mining](erpcm-recommendations-and-similar-candidates.md)**  
The record for each candidate in ERP Semantic Mining displays information on suggested next steps and similar candidates to help you in replatforming an ERP \(Enterprise Resource Planning\) app.
-   **[Next steps when replatforming apps to ServiceNow using ERP Semantic Mining](ecm-next-steps-replatforming.md)**  
After you use ERP Semantic Mining to identify legacy ERP \(Enterprise Resource Planning\) candidates, use additional ServiceNow AI Platform products and resources to replatform your app.
-   **[Guided tours in ERP Semantic Mining](guided-tours-in-erp-customization-mining.md)**  
Learn about ERP Semantic Mining guided tours, including how to access and take them to build your knowledge of ERP Semantic Mining.
-   **[Get help with ERP Semantic Mining](erp-customization-mining-get-help-now.md)**  
For help with ERP Semantic Mining, contact the ServiceNow admin who works in your organization.

**Parent Topic:**[ERP Semantic Mining](erp-customization-mining-overview.md)

