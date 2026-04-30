---
title: Discovery models and software installations
description: Software discovery models are automatically created during discovery to identify and normalize the software installed in your environment.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Discovery models and software installations

Software discovery models are automatically created during discovery to identify and normalize the software installed in your environment.

Software discovery models are stored in the Software Discovery Model \[cmdb\_sam\_sw\_discovery\_model\] table. The normalization process is automatically run when a new discovery model is created. Discovery models are not created for software installations that have a name containing `Security Update`.

There is a difference between [software models](software-models-and-entitlements.md) and software discovery models.

-   A software model is a specific version or configuration of software that is purchased and/or available to users.
-   A software discovery model is a model created when a version of software is discovered in a network environment.

Multiple software discovery models can be associated to one software model. For example, a software model can be defined as follows:

-   Publisher = X
-   Product = Y
-   Version = Starts with 10

If there are two separate installs of this product \(version 10.1 and version 10.2\), two discovery models are created. One of the discovery models has the discovered version set to 10.1, and the other discovery model has the discovered version set to 10.2. The reconciliation process associates both of these discovery models to the same software model since they both meet the version criterion of `Starts with 10`.

## Discovery Models

Software discovery models cannot be created manually. The following field combination, called the primary key, is used to match new software installations to a new or existing software discovery model.

Primary key: **Publisher**, **Display Name**, and **Version**

**Note:** When analyzing version numbers, an exact match is always searched for first, but rounds down to a major version number when an exact match is not found.

For example, if no match is found for version number 8.0.4, but version 8.0 is found, then version 8.0 is used in the **Software model** field.

**Note:** If normalized field values differ from the values in the package or pattern, a caution icon is indicated next to the Normalization status field indicating that a normalization suggestion record has been created. Clicking the caution icon opens the [Normalization Suggestion](../task/view-norm-suggestions-sam.md) record for that discovery model.

The differing values can be set by the user, or by accepting the normalization suggestion changes. Once a new value is set, the normalization status changes form Normalized to Manually Normalized.

Under specific conditions, certain fields that are typically read-only can be edited. If edited, the status changes to Manually Normalized.

## Revert normalization

You can revert a normalization if needed.

When you revert a normalization, discovery models that have a status of **Normalized**, **Partially Normalized**, or **Publisher Normalized** revert to the status of **Match Not Found**. All normalized fields are also reset to their original unnormalized values. You can then normalize your discovery models manually or wait for the next normalization to run automatically. If you are normalizing your discovery models manually, the Software Asset Management application creates normalization suggestions based on the latest normalization rules from the Content Service team. You can choose to accept or reject these suggestions. If you wait for normalization to run automatically, discovery models are normalized using the latest normalization rules from the Content Service team. The discovery models are then set to a status of **Normalized**, **Partially Normalized**, or **Publisher Normalized**, and the normalized field values are set.

## Software Installations

The Software Installations list contains the software installed in your organization and is populated by discovery.

Installed software is placed in the Software Installation \[cmdb\_sam\_sw\_install\] table by Discovery, and a primary key is built \(using **Publisher**, **Display Name**, and **Version** fields\).

Discovery automatically matches the discovered software installation with a new or existing software discovery model using the primary key.

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

