---
title: Map the taxonomy
description: Create an internal taxonomy when you are setting up the Regulatory Change Management application. Map the external taxonomy to the internal taxonomy so that the Regulatory Change Management application refers to only one taxonomy.
locale: en-US
release: australia
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Set up the RSS feeds infrastructure, Configure, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Map the taxonomy

Create an internal taxonomy when you are setting up the Regulatory Change Management application. Map the external taxonomy to the internal taxonomy so that the Regulatory Change Management application refers to only one taxonomy.

## Before you begin

Role required: sn\_grc\_reg\_change.admin

## About this task

The Regulatory Change Management application stores the taxonomy and it provides a way to map the taxonomies using the UI component.

## Procedure

1.  Navigate to **Application** &gt; **Regulatory Change Management** &gt; **Taxonomy** &gt; **Taxonomy Classes**.

    The pre-defined taxonomy classes are displayed:

    -   Content Types- Content types provide site-specific control of how system data defined by templates is rendered.
    -   Jurisdictions- Jurisdictions in regions are used for data breach notification obligations as each obligation is broken down by jurisdiction.
    -   Regulatory Bodies- Regulatory bodies that govern the regulations. For example, RBI, SEBI, SEC, TRRI, and so on.
    -   Sectors- Sectors businesses that are governed by government rules. For example, FRM, FDIC, SEC.
    -   Themes- Themes indicate the ares that organisations should consider in their regulatory change management.
2.  Navigate to the following taxonomy tables if you want to view or update the taxonomy class name:

    -   **Content Types**
    -   **Jurisdictions**
    -   **Regulatory Bodies**
    -   **Sectors**
    -   **Themes**
    As an example, when you select Jurisdiction, the Class name field displays Jurisdiction as the taxonomy class.

    **Note:** Only users with the sn\_grc\_reg\_change.admin roles can update the taxonomy tables.

3.  Select **Update** to update the class name.

4.  Select **New** under Taxonomy class related list.

    A new Taxonomy class record is displayed on a separate page.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the taxonomy class.|

    The new taxonomy class is displayed on the Taxonomy Class page.

5.  Open the Taxonomy Class page to create a new Taxonomy class mapping record.

6.  On the form, fill in the fields.

    Depending on what regulatory table was previously selected, the form title is different.

    |Field|Description|
    |-----|-----------|
    |Provider|Provider of the alerts.|
    |External taxonomy class|External taxonomy class that is mapped with the internal taxonomy class.|
    |Taxonomy class|Taxonomy class provided by default such as Jurisdictions or Content type.|

7.  Select **Submit** to map the external taxonomy class to the internal taxonomy class.

    The external taxonomy class is mapped to the internal taxonomy class.


