---
title: Installing Data Classification plugin demo data
description: When you upgrade to or install Zurich \(and above\), the Data Classification \(com.glide.data\_classification\) plugin is automatically activated. However, you should manually install the demo data that comes with the plugin. It includes several important pre-defined data classifications, and it also assigns one of them to specific User \[sys\_user\] table columns in your instance.When you install the demo data included in the Data Classification \(com.glide.data\_classification\) plugin, several types of components are installed in your instance. These components include pre-defined data classifications and code assignments for specific User \[sys\_user\} columns.
locale: en-US
release: zurich
product: Data Classification
classification: data-classification
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Data Classification, Platform Privacy]
---

# Installing Data Classification plugin demo data

When you upgrade to or install Zurich \(and above\), the Data Classification \(com.glide.data\_classification\) plugin is automatically activated. However, you should manually install the demo data that comes with the plugin. It includes several important pre-defined data classifications, and it also assigns one of them to specific User \[sys\_user\] table columns in your instance.

## Before you begin

Role required: admin

## About this task

Regardless of whether you install demo data, the activated Data Classification plugin adds the following user roles in your instance:

-   data\_classification\_admin: Can administer all aspects of the Data Classification application, including data classification setup and assignment.
-   data\_classification\_auditor: Can audit Data Classification code assignments made to user tables and columns.

**Important:** Notice regarding use by Customers:

All decisions in connection with the implementation of this application are at the sole decision of the Customer. Customers acknowledge and agree that use of the application is not a representation by ServiceNow of compliance with any law or regulation and any suggested language, field or classification provided out of the box with the application does not constitute legal advice by ServiceNow.

Customers remain solely responsible for complying with their legal obligations under applicable law, including \(but not limited to\) data protection, security requirements, and privacy laws, and are responsible for configuring and making any necessary modifications to this application, including \(but not limited to\) templates, to meet the Customers’ requirements.

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Data Classification plugin using the filter criteria and search bar.

    An `Installed` message appears after you locate the plugin.

3.  Click the icon with three vertical dots, then select **Repair** to access the Activate Plugin dialog.

4.  Select **Load demo data**, and then click **Repair**.


## Components installed with Data Classification demo data

When you install the demo data included in the Data Classification \(com.glide.data\_classification\) plugin, several types of components are installed in your instance. These components include pre-defined data classifications and code assignments for specific User \[sys\_user\} columns.

### Data Classifications installed

|data classification|Description|
|-------------------|-----------|
|Confidential|Sensitive data that if compromised could negatively affect operations.|
|Internal|Internal data not meant for public disclosure.|
|Personally Identifiable Information|Also known as PII. Data that could potentially be used to identify a particular person.|
|Public|Data that may be freely disclosed to the public.|
|Restricted|Highly sensitive corporate data that if compromised could put the organization at financial or legal risk.|

### Data Classification assignments

|Table|Assigned Column|Assigned data classification|
|-----|---------------|----------------------------|
|sys\_user|zip|Personally identifiable information|
|sys\_user|first\_name|Personally identifiable information|
|sys\_user|email|Personally identifiable information|
|sys\_user|city|Personally identifiable information|
|sys\_user|middle\_name|Personally identifiable information|
|sys\_user|street|Personally identifiable information|
|sys\_user|mobile\_phone|Personally identifiable information|
|sys\_user|last\_name|Personally identifiable information|
|sys\_user|country|Personally identifiable information|
|sys\_user|gender|Personally identifiable information|
|sys\_user|name|Personally identifiable information|
|sys\_user|photo|Personally identifiable information|
|sys\_user|state|Personally identifiable information|
|sys\_user|home\_phone|Personally identifiable information|

