---
title: Exploring Data Privacy
description: Use Data Privacy to classify sensitive data and to remove personally identifiable information \(PII\) from user data in a production instance and anonymize data in non-production instances. Once anonymized, the user data is no longer considered regulated private information.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Platform Privacy]
---

# Exploring Data Privacy

Use Data Privacy to classify sensitive data and to remove personally identifiable information \(PII\) from user data in a production instance and anonymize data in non-production instances. Once anonymized, the user data is no longer considered regulated private information.

Explains the importance of data privacy and the steps businesses can take to protect sensitive information through classification and anonymization. Using the Data Privacy store application, we give an overview of the main dashboard and capabilities.

Developers must work with data on non-production instances to ensure that their implementations are working as expected. While importing data from your production instance is a useful way to simulate production, it presents a security risk. Administrators can use data privacy to provide developers with data that does not contain private information to work safely in a non-production environment.

## Data classification

Identify and classify your sensitive data according to pre-defined criteria determined by the level of sensitivity of the data types in your instance. Data sensitivity levels help determine how each type of classified data should be handled. There are several pre-defined classes provided with base level data privacy. Use the classification section of Data Privacy to label and group data within your instance. Add classes, view data class structure and classify data. Group data by type, using pre-defined or user-defined data classifications.

Explains how to classify data using the Data Privacy store application.

## User data anonymization

As an administrator, you define whether to anonymize all information for all users or for a subset of users. When anonymized, data for the selected user records is replaced with randomized values or values you define. When replacing values, the data structure can be preserved using various techniques.

Explains how to anonymize data using the Data Privacy store application.

## Data privacy options

-   [Data privacy \(Classic\)](../reference/data-privacy-classic.md): First use the data classification app to group your data by type, using pre-defined or user-defined data classifications. Then create data privacy techniques and jobs to anonymize PII.
-   [Data privacy](../../data-privacy-store/concept/dps-data-privacy.md) \(Store App\): Classify and anonymize your data all from within the data privacy app.

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

-   Only classified data can be anonymized. For information on data classes and classification, see [Data classification](data-classification.md) \(Classic\) or [Data classification](../../data-privacy-store/concept/dps-data-classification.md) Store App.
-   PII in logs and other auditing data are not anonymized.
-   Only structured data can be anonymized. Unstructured data, such as Journal fields, comments, attachments, and other fields where partial text may represent PII is not anonymized. See [Supported field types for anonymization](../reference/data-privacy-supported-data-types.md) for more information.
-   Integrations with single sign-on \(SSO\) systems may resynchronize user information from their source of truth systems. There is no mechanism in place to ensure the permanency of the de-identification of sys\_user data. For information on user administration and sys\_users see [User Administration](https://www.servicenow.com/docs/access?context=c_UserAdministration&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

