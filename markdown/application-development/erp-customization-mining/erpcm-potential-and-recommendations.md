---
title: How ERP Customization Mining determines candidate score and potential
description: ERP Customization Mining \(ERP-CM\) generates a score to rank the potential for replatforming legacy ERP \(Enterprise Resource Planning\) candidates onto the ServiceNow AI Platform.
locale: en-US
release: xanadu
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exploring ERP Customization Mining, ERP Customization Mining \(ERP-CM\), Building low-code applications, Developing your application, Building applications]
---

# How ERP Customization Mining determines candidate score and potential

ERP Customization Mining \(ERP-CM\) generates a score to rank the potential for replatforming legacy ERP \(Enterprise Resource Planning\) candidates onto the ServiceNow AI Platform.

Every candidate has an ERP module specified in the candidate details in ERP-CM. The ERP module is used to evaluate the potential score of the candidate for replatforming, as well as the remote tables and extraction tables the model contains.

-   Remote tables get their records from running an associated script against an external data source.
-   Extraction tables retrieve large amounts of data using a scheduled query, and use transform tables to process data for use on the ServiceNow AI Platform.

**Note:**

Admins must first configure the connection to the ERP system in ERP Data Hub. For more information, see [Working with ERP systems in ERP Data Hub](../../erp-integration/concept/erp-canvas-work-with-systems.md).

## High and low scores for candidate potential

ERP-CM evaluates candidates based on how well their tables and fields are supported by the ServiceNow AI Platform.

-   A high potential indicates that ERP-CM can immediately use remote tables and extraction tables that match the ERP model for the application candidate without making additional changes.
-   A low potential indicates that the application candidate matches few of the remote tables and extraction tables in the ERP models in ERP Data Hub.

## How scores are calculated

The candidate potential score is calculated using the following metrics:

-   ERP models: The number of ERP models that the candidate uses remote tables and extraction tables from.
-   Similar candidates: The number of candidates with a similarity score above the threshold, which accounts for both table-based similarity and model-based similarity.

    The threshold can be adjusted in the System Properties \[sys\_properties\] table, and the default `OR` condition can be changed to `AND`.

-   Supported table score: The ratio of the number of custom app tables that are supported by any ERP model relative to the number of custom app tables.

    **Note:** Tables from either the Technical or ServiceNow table clusters are ignored from these computations.

-   Supported table usage: The ratio of tables supported by the relevant ERP models that are used by the custom app.
-   Unsupported model penalty: A penalty for the number of unsupported operations on tables in ERP models. The number of unsupported operations is passed through a sigmoid function, so it ranges from 0.0 and 1.0.
-   Unsupported table extensions: The number of custom app tables that are also suggested as model extensions.
-   Model inaccuracy: The number of tables supported by relevant ERP models that aren’t used by custom apps, and are passed through a sigmoid function.

**Parent Topic:**[Exploring ERP Customization Mining](exploring-ecm.md)

