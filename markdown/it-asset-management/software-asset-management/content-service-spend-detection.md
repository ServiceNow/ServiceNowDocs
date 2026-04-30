---
title: Content Service for Software Spend Detection
description: Opt in to Software Asset Management Content Service for Software Spend Transactions to get more accurate predictions in Software Spend Detection by sharing financial transaction data with the ServiceNow Content Service team.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Opt in to Content Service, Software Spend Detection, Software Asset Management, IT Asset Management]
---

# Content Service for Software Spend Detection

Opt in to Software Asset Management Content Service for Software Spend Transactions to get more accurate predictions in Software Spend Detection by sharing financial transaction data with the ServiceNow Content Service team.

Opting in to Content Service for Software Spend Transactions means that you agree to have a copy of your financial transaction data securely sent to the ServiceNow Content Service team. ServiceNow uses your data only to improve future publisher and product predictions when importing data into Software Spend Detection. ServiceNow protects all data using the same policies that protect customer instances.

Opting-in shares the following data with ServiceNow:

-   Vendor name
-   Transaction description
-   GL account
-   Prediction results \(Publisher ID, Product ID, Is Software\)

Your data is sent anonymously to the Content Service team. Your data isn't linked to any identifiable information, such as company or instance name. Before importing data, it's your responsibility to ensure that the fields **Vendor name**, **Transaction Description**, and **GL account** don't contain any identifiable information such as company or employee names.

The ServiceNow Content Service team uses these data points to improve machine learning models used by ServiceNow Artificial Intelligence \(AI\) Services. The AI Services are a set of web services that reside within every ServiceNow datacenter. All Software Spend Detection users benefit from continual improvements to ServiceNow AI Services, but users who are opted-in to Content Service benefit the most. ServiceNow AI Services learns how to identify software products and publishers in your transactions that Software Spend Detection previously was not able to identify. This learning improves the functionality for your future imports.

![Data flow in Content Service.](../image/spend-content-service.png)

You can opt out of Content Service at any time. If you opt out, no data from future imports is sent to the ServiceNow Content Service team, but your previously shared data is not deleted. If you would like to participate in Content Service but exclude some transactions from being shared with ServiceNow, you can select the **Exclude from content service** check box on those transaction records.

**Parent Topic:**[Opt in to Content Service](../task/opt-in-content-service.md)

