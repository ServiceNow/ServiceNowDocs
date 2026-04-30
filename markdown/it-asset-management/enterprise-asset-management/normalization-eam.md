---
title: Enterprise Asset Management normalization
description: The Enterprise Asset Management normalization process enables you to normalize your manufacturer, model name, model number, and model type data of your enterprise models.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Explore, Enterprise Asset Management, IT Asset Management]
---

# Enterprise Asset Management normalization

The Enterprise Asset Management normalization process enables you to normalize your manufacturer, model name, model number, and model type data of your enterprise models.

## Normalization overview

The normalization process compares the discovered manufacturer, discovered model, discovered model type, and the discovered model number values against the ServiceNow repository of normalized equivalents in the Enterprise Asset Management Content Service.

To standardize your enterprise models, the data must be normalized. You can manually update the model records with the normalization content, or you can compare your data against the Enterprise Asset Management Content Service.

## Scheduled jobs for Normalization

The following are the scheduled jobs that run during the normalization process.

<table id="table_u2f_qj1_vtb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

EAM - Daily Job

</td><td>

Sets the time when data is pulled by the Enterprise Asset Management Content Service. This job runs only once, when the normalization process is started for the first time.

 If a model has gone beyond its end of its lifecycle date, this job enables the **Content lifecycle phase** check box in the **Enterprise Model Lifecycle** tab in a model record.

</td></tr><tr><td>

EAM - Content Upload

</td><td>

A daily job that uploads any content to the Enterprise Asset Management Content Service that you have added in the following custom tables:-   Custom Enterprise Model Type \[sn\_eam\_cd\_custom\_model\_type\]
-   Custom Enterprise Manufacturer \[sn\_eam\_cd\_custom\_manufacturer
-   Custom Enterprise Product Model \[sn\_eam\_cd\_custom\_product\_model\]
-   Custom Enterprise Model Library \[sn\_eam\_cd\_custom\_model\_library\]

 **Note:** This job only runs if you have opted in to the Enterprise Asset Management Content Service.

</td></tr><tr><td>

EAM - Enterprise Lifecycles

</td><td>

Updates the model record with information about newly created or deleted life cycles.

</td></tr><tr><td>

EAM - Normalization

</td><td>

Normalizes all the models that haven't been normalized.

</td></tr><tr><td>

EAM - Apply latest content changes

</td><td>

Updates any changes in the content tables to the Enterprise Asset Management Content Service.

</td></tr></tbody>
</table>## Tables installed with Enterprise Asset Management normalization

Several normalization tables are installed with the activation of the Enterprise Asset Management application.

|Table|Description|
|-----|-----------|
|Custom Enterprise Model Type \[sn\_eam\_cd\_custom\_model\_type\]|Stores custom enterprise model type records.|
|Custom Enterprise Manufacturer \[sn\_eam\_cd\_custom\_manufacturer\]|Stores custom enterprise manufacturer records.|
|Custom Enterprise Product Model \[sn\_eam\_cd\_custom\_product\_model\]|Stores custom enterprise product model records.|
|Custom Enterprise Model Library \[sn\_eam\_cd\_custom\_model\_library\]|Stores enterprise model library records.|
|Enterprise Model Type \[sn\_eam\_cd\_model\_type\]|Stores enterprise model type records.|
|Enterprise Manufacturer \[sn\_eam\_cd\_manufacturer\]|Stores enterprise model manufacturer records.|
|Enterprise Product Model \[sn\_eam\_cd\_product\_model\]|Stores enterprise product model records.|
|Enterprise Model Library \[sn\_eam\_cd\_model\_library\]|Stores enterprise model library records.|
|Enterprise Lifecycle Definition \[sn\_eam\_cd\_lifecycle\_definition\]|Stores lifecycle phase of an enterprise model and associated dates.|
|EAM Content Audit \[sn\_eam\_content\_audit\]|Stores the content values that changed.|
|Manage Enterprise Library \[sn\_eam\_manage\_cd\_library\]|Stores import and export content data.|
|Enterprise Asset Configurations \[sn\_eam\_configuration\]|Stores opt-in and opt-out data.|

