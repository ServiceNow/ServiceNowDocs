---
title: Types of differences between CDM applications
description: Descriptions and examples of differences between CDM applications when using the Config Data Analyzer tool.
locale: en-US
release: australia
product: DevOps \(Family\)
classification: devops-family
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Compare config data of two CDM applications, Using DevOps Config, DevOps Config, IT Service Management]
---

# Types of differences between CDM applications

Descriptions and examples of differences between CDM applications when using the Config Data Analyzer tool.

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

## Types of differences

On the **App compare** tab, the **CDIs and variables** tab displays changes to individual CDIs for the node that is selected in the navigation panel. The **Description** column displays one of the following values that describes how the changesets differ.

-   **Values are different**

    Both the reference and target changesets include a particular CDI, but the values differ between the two changesets. See the **Reference** and **Target** columns for the values.

-   **Encryption settings are different**

    The **View encrypted data** setting is selected for one changeset and not selected for the other changeset.

    **Note:** For users that do not have the CDM Secrets \[sn\_cdm.cdm\_secrets\] role, encrypted data always appears as \*\*\*\*\*\*\*\*.

-   **Source levels are different**

    One of the following cases:

    -   The value is direct in one changeset and is overridden in the other changeset.
    -   The value is direct in one changeset and is included in the other changeset.
-   **Source levels and values are different**

    In addition to the cases described in "Source levels are different", the value differs between changesets.

-   **Target only**

    A CDI or the value for a CDI appears only in the target changeset.

-   **Reference only**

    A CDI or the value for a CDI appears only in the reference changeset.


## Examples of differences

![Examples of differences between changesets, part 1](../image/cdm-cda-diff-types1.png)

![Examples of differences between changesets, part 2](../image/cdm-cda-diff-types2.png)

