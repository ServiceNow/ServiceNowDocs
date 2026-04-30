---
title: Information objects in Privacy Management
description: The purpose of an information object is to logically describe the type of data that is exchanged between an application and a database.
locale: en-US
release: zurich
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Explore, Privacy Management, Governance, Risk, and Compliance]
---

# Information objects in Privacy Management

The purpose of an information object is to logically describe the type of data that is exchanged between an application and a database.

To determine which information objects process personal data, you can classify the information objects as **Personal information**. For more details on how to classify an information object, see [Classify information objects as personal information](../task/tag-io-with-pi.md).

After the information objects are created, they are mapped to business applications or business processes. This activity helps the privacy management teams to discover the information objects processing personal data. Some examples of \[PI\] Information objects in Privacy Management are:

-   Email addresses
-   Bank account numbers
-   Educational details
-   Personal email address

## Creation of information object categories

Information object categories provide a systematic way to classify information objects, making it easier to align with regulatory requirements. For instance, regulators often group attributes like iris scans and fingerprints under the category of biometric data. Similarly, email addresses and phone numbers are commonly categorized as contact information. While regulators focus on these broad classifications, business users typically refer to the individual data elements rather than the overarching category. In such scenarios, information object categories serve as a framework to organize and classify these data elements into their respective broader categories.

Also, if the regulators identify a new data element for a certain category, then the privacy administrator simply needs to add the data element to the data category and all the assessments are refreshed. This ability helps save time and you do not have to manually add the new information objects to the assessments. For information on how to configure information object categories, see [Configure information object categories](../task/configure-information-object-categories.md).

You can create information objects manually. See [Create an information object](../task/create-information-object.md).

**Parent Topic:**[Exploring Privacy Management](explore-privacy-management.md)

