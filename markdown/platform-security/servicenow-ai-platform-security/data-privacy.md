---
title: Exploring Data Privacy
description: Use Data Privacy to classify sensitive data and to remove personally identifiable information \(PII\) from user data in a production instance and anonymize data in non-production instances. Once anonymized, the user data is no longer considered regulated private information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-security/servicenow-ai-platform-security/data-privacy.html
release: zurich
product: ServiceNow AI Platform Security
classification: servicenow-ai-platform-security
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Platform Privacy]
---

# Exploring Data Privacy

Use Data Privacy to classify sensitive data and to remove personally identifiable information \(PII\) from user data in a production instance and anonymize data in non-production instances. Once anonymized, the user data is no longer considered regulated private information.

Developers must work with data on non-production instances to ensure that their implementations are working as expected. While importing data from your production instance is a useful way to simulate production, it presents a security risk. Administrators can use data privacy to provide developers with data that does not contain private information to work safely in a non-production environment.

## Data classification

Identify and classify your sensitive data according to pre-defined criteria determined by the level of sensitivity of the data types in your instance. Data sensitivity levels help determine how each type of classified data should be handled. There are several pre-defined classes provided with base level data privacy. Use the classification section of Data Privacy to label and group data within your instance. Add classes, view data class structure and classify data. Group data by type, using pre-defined or user-defined data classifications.

## User data anonymization

As an administrator, you define whether to anonymize all information for all users or for a subset of users. When anonymized, data for the selected user records is replaced with randomized values or values you define. When replacing values, the data structure can be preserved using various techniques.

## Data Privacy

Use [Data privacy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/data-privacy-classic/dps-data-privacy.md) to classify sensitive data and to remove personally identifiable information \(PII\) from user data in a production instance and anonymize data in non-production instances.

**Note:** You can also use the legacy plugin [Data privacy \(Classic\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/data-privacy-classic/data-privacy-classic.md).

## Installation details

You must have the following applications installed on your instance:

-   Data Privacy \(Classic\) \[com.glide.data\_privacy\]
-   Data Privacy \[sn\_dp\_store\_app\]
-   Data Discovery \[sn\_data\_discovery\]
-   Data Discovery APIs\[com.glide.data\_discovery\]

Here is the how the installation works:

-   Installing the Data Privacy Store App will auto install the Data Discovery Store App, Data Privacy \(Classic\) plug-in, and the Data Classification plugin.
-   Installing the Data Discovery Store App will auto install the Data Discovery APIs plugin

## Considerations

-   Only classified data can be anonymized. For information on data classes and classification, see [Data classification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/data-classification/data-classification.md) \(Classic\) or [Data classification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/data-privacy-classic/dps-data-classification.md) Store App.
-   PII in logs and other auditing data are not anonymized.
-   Only structured data can be anonymized. Unstructured data, such as Journal fields, comments, attachments, and other fields where partial text may represent PII is not anonymized. See [Supported field types for anonymization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-security/data-privacy-classic/data-privacy-supported-data-types.md) for more information.
-   Integrations with single sign-on \(SSO\) systems may resynchronize user information from their source of truth systems. There is no mechanism in place to ensure the permanency of the de-identification of sys\_user data. For information on user administration and sys\_users see [User Administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/user-administration/c_UserAdministration.md).

